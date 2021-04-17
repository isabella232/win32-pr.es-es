---
description: En la información de Resumen de un paquete de instalación, la propiedad de Resumen de recuento de palabras indica el tipo de imagen del archivo de origen.
ms.assetid: 1eeece25-4f24-4efe-879d-66ebbb6a9391
title: Propiedad de Resumen de recuento de palabras
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c4200cb946f6948770d0c900c2df651b8fbff11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653667"
---
# <a name="word-count-summary-property"></a>Propiedad de Resumen de recuento de palabras

En la información de Resumen de un paquete de instalación, la propiedad de **Resumen de recuento de palabras** indica el tipo de imagen del archivo de origen. Si esta propiedad no está presente, el valor predeterminado es cero (0).

Esta propiedad es un campo de bits. Se pueden agregar nuevos bits en el futuro. En la actualidad, están disponibles los bits siguientes.



| bit   | Value          | Descripción                                                                                                                                                                                                                                      |
|-------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bit 0 | 0 1<br/> | Nombres de archivo largos. Nombres de archivo cortos.<br/>                                                                                                                                                                                                    |
| Bit 1 | 0 2<br/> | El origen está descomprimido. El origen está comprimido.<br/>                                                                                                                                                                                         |
| Bit 2 | 0 4<br/> | El origen es el medio original. El origen es una imagen administrativa creada por una instalación administrativa.<br/>                                                                                                                                 |
| Bit 3 | 0 8<br/> | Los privilegios elevados pueden ser necesarios para instalar este paquete. No se necesitan privilegios elevados para instalar este paquete.<br/> Disponible a partir de Windows Installer versión 4,0 y Windows Vista o Windows Server 2008.<br/> |



 

Se combinan para proporcionar a la propiedad de **Resumen de recuento de palabras** uno de los siguientes valores que indican un tipo de imagen de archivo de origen.



| Value | Tipo                                                                                                                                                                                                                                                                                            |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Origen original usando nombres de archivo largos. Coincide con el árbol de la [tabla de directorios](directory-table.md). Los privilegios elevados pueden ser necesarios para instalar este paquete.                                                                                                                                     |
| 1     | Origen original usando nombres de archivo cortos. Coincide con el árbol de la [tabla de directorios](directory-table.md). Los privilegios elevados pueden ser necesarios para instalar este paquete.                                                                                                                                    |
| 2     | Archivos de código fuente comprimidos con nombres de archivo largos. Coincide con los archivadores y archivos de la [tabla de medios](media-table.md). Los privilegios elevados pueden ser necesarios para instalar este paquete.                                                                                                                   |
| 3     | Archivos de código fuente comprimidos con nombres de archivo cortos. Coincide con los archivadores y archivos de la [tabla de medios](media-table.md). Los privilegios elevados pueden ser necesarios para instalar este paquete.                                                                                                                  |
| 4     | Imagen administrativa que usa nombres de archivo largos. Coincide con el árbol de la [tabla de directorios](directory-table.md). Los privilegios elevados pueden ser necesarios para instalar este paquete.                                                                                                                                |
| 5     | Imagen administrativa que usa nombres de archivo cortos. Coincide con el árbol de la [tabla de directorios](directory-table.md). Los privilegios elevados pueden ser necesarios para instalar este paquete.                                                                                                                               |
| 8     | No se necesitan privilegios elevados para instalar este paquete. Use este valor al [crear paquetes sin el cuadro de diálogo de UAC](authoring-packages-without-the-uac-dialog-box.md). Disponible a partir de Windows Installer versión 4,0 y Windows Vista o Windows Server 2008.<br/> |



 

Tenga en cuenta que si el paquete está marcado como comprimido (bit 1 está establecido), el Windows Installer solo instala los archivos que se encuentran en la raíz del origen. En este caso, incluso los archivos marcados como sin comprimir en la [tabla de archivos](file-table.md) deben encontrarse en la raíz que se va a instalar. Para especificar una imagen de origen que tenga un archivo. cab (archivos comprimidos) y archivos sin comprimir que coincidan con el árbol en la [tabla de directorios](directory-table.md), marque el paquete como descomprimido; para ello, deje bit 1 sin establecer (valor = 0) en la propiedad de **Resumen de recuento de palabras** y establezca **msidbFileAttributesCompressed** (Value = 16384) en la columna Attributes de la [tabla File](file-table.md)

En una transformación, la propiedad de **Resumen de recuento de palabras** debe ser null.

En el flujo de información de Resumen de un paquete de revisión, la propiedad de **Resumen de recuento de palabras** indica la versión mínima Windows Installer necesaria para instalar la revisión.



| Value | Significado                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | El valor predeterminado, que indica que MSPATCH se usó para crear la revisión.                                                                                                        |
| 2     | Requiere como mínimo Windows Installer 1,2 para que se aplique la revisión. Una revisión con un recuento de palabras de "2" produce un error inmediatamente si se usa con una versión de Windows Installer anterior a la 1,2. |
| 3     | Requiere como mínimo Windows Installer 2,0 para que se aplique la revisión. Una revisión con un recuento de palabras de "3" produce un error inmediatamente si se usa con una versión de Windows Installer anterior a la 2,0. |
| 4     | Requiere como mínimo Windows Installer 3,0 para que se aplique la revisión. Se produce un error en una revisión con un recuento de palabras de "4" si se usa con una versión de Windows Installer anterior a la 3,0.             |
| 5     | Requiere como mínimo Windows Installer 3,1 para que se aplique la revisión.                                                                                                               |



 

Esta propiedad de resumen es obligatoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Descripciones de propiedades de Resumen](summary-property-descriptions.md)
</dt> </dl>

 

 




