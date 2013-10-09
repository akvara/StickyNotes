StickyNotes
===========

Tutorial
--------
http://bigemployee.com/zend-framework-2-simple-web-application-crud-using-ajax-tutorial/

Base setup
----------
CREATE DATABASE IF NOT EXISTS `stickynotes` DEFAULT CHARACTER SET utf8  DEFAULT COLLATE utf8_general_ci;
USE `stickynotes`;
CREATE USER 'www-data'@'localhost' IDENTIFIED BY 'www-data';
GRANT ALL PRIVILEGES ON `stickynotes` . * TO 'www-data'@'localhost';

DROP TABLE IF EXISTS `stickynotes`.`stickynotes` ;
CREATE TABLE IF NOT EXISTS `stickynotes`.`stickynotes` (
`id` INT NOT NULL AUTO_INCREMENT ,
`note` VARCHAR(255) NULL ,
`created` TIMESTAMP NOT NULL ,
PRIMARY KEY (`id`) ,
UNIQUE INDEX `id_UNIQUE` (`id` ASC) )
ENGINE = MyISAM;
-- -----------------------------------------------------
-- Data for table `stickynotes`.`stickynotes`
-- -----------------------------------------------------
START TRANSACTION;
USE `stickynotes`;
INSERT INTO `stickynotes`.`stickynotes` (`id`, `note`, `created`) VALUES (NULL, 'This is a sticky note you can type and edit.', NULL);
INSERT INTO `stickynotes`.`stickynotes` (`id`, `note`, `created`) VALUES (NULL, 'Lets see if it will work with my iPhone', NULL);
COMMIT;
