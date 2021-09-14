---
description: En la información de resumen de un paquete de instalación, la propiedad Resumen de recuento de palabras indica el tipo de imagen de archivo de origen.
ms.assetid: 1eeece25-4f24-4efe-879d-66ebbb6a9391
title: Propiedad Resumen de recuento de palabras
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c4200cb946f6948770d0c900c2df651b8fbff11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246369"
---
# <a name="word-count-summary-property"></a>Propiedad Resumen de recuento de palabras

En la información de resumen de un paquete de instalación, la propiedad **Resumen** de recuento de palabras indica el tipo de imagen de archivo de origen. Si esta propiedad no está presente, el valor predeterminado es cero (0).

Esta propiedad es un campo de bits. En el futuro se pueden agregar nuevos bits. En la actualidad, están disponibles los siguientes bits.



| bit   | Value          | Descripción                                                                                                                                                                                                                                      |
|-------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bit 0 | 0 1<br/> | Nombres de archivo largos. Nombres de archivo cortos.<br/>                                                                                                                                                                                                    |
| Bit 1 | 0 2<br/> | El origen está descomprimido. El origen está comprimido.<br/>                                                                                                                                                                                         |
| Bit 2 | 0 4<br/> | El origen es un medio original. El origen es una imagen administrativa creada por una instalación administrativa.<br/>                                                                                                                                 |
| Bit 3 | 0 8<br/> | Se pueden tener privilegios elevados para instalar este paquete. No se requieren privilegios elevados para instalar este paquete.<br/> Disponible a partir de Windows Installer versión 4.0 y Windows Vista o Windows Server 2008.<br/> |



 

Se combinan para proporcionar a la **propiedad Resumen de recuento** de palabras uno de los siguientes valores que indican un tipo de imagen de archivo de origen.



| Value | Tipo                                                                                                                                                                                                                                                                                            |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Origen original con nombres de archivo largos. Coincide con el árbol de [la tabla de directorios](directory-table.md). Se pueden tener privilegios elevados para instalar este paquete.                                                                                                                                     |
| 1     | Origen original con nombres de archivo cortos. Coincide con el árbol de [la tabla de directorios](directory-table.md). Se pueden tener privilegios elevados para instalar este paquete.                                                                                                                                    |
| 2     | Archivos de origen comprimidos mediante nombres de archivo largos. Coincide con los archivos y los archivadores de [la tabla multimedia](media-table.md). Se pueden tener privilegios elevados para instalar este paquete.                                                                                                                   |
| 3     | Archivos de origen comprimidos mediante nombres de archivo cortos. Coincide con los archivos y los archivadores de [la tabla multimedia](media-table.md). Se pueden tener privilegios elevados para instalar este paquete.                                                                                                                  |
| 4     | Imagen administrativa con nombres de archivo largos. Coincide con el árbol de [la tabla de directorios](directory-table.md). Se pueden tener privilegios elevados para instalar este paquete.                                                                                                                                |
| 5     | Imagen administrativa con nombres de archivo cortos. Coincide con el árbol de [la tabla de directorios](directory-table.md). Se pueden tener privilegios elevados para instalar este paquete.                                                                                                                               |
| 8     | No se requieren privilegios elevados para instalar este paquete. Use este valor al [crear paquetes sin el cuadro de diálogo UAC](authoring-packages-without-the-uac-dialog-box.md). Disponible a partir Windows Installer versión 4.0 y Windows Vista o Windows Server 2008.<br/> |



 

Tenga en cuenta que si el paquete está marcado como comprimido (se establece el bit 1), Windows Installer solo instala los archivos ubicados en la raíz del origen. En este caso, incluso los archivos marcados como sin comprimir en la tabla [de](file-table.md) archivos deben encontrarse en la raíz para instalarse. Para especificar una imagen de origen que tenga un archivo contenedor (archivos comprimidos) y archivos sin comprimir que coincidan con el árbol de  la tabla de directorios [,](directory-table.md)marque el paquete como sin comprimir dejando bit 1 [](file-table.md) sin establecer (valor = 0) en la propiedad Resumen de recuento de palabras y establezca **msidbFileAttributesCompressed** (valor =16384) en la columna Atributos de la tabla de archivos para cada archivo del archivador.

En una transformación, la **propiedad Resumen del recuento de palabras** debe ser Null.

En el flujo de información de  resumen de un paquete de revisión, la propiedad Resumen de recuento de palabras indica la versión mínima del instalador Windows necesaria para instalar la revisión.



| Value | Significado                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Valor predeterminado, que indica que se usó MSPATCH para crear la revisión.                                                                                                        |
| 2     | Requiere como mínimo Windows Installer 1.2 para que se aplique la revisión. Se produce un error inmediatamente en una revisión con un recuento de palabras de "2" si se usa con una Windows installer anterior a la 1.2. |
| 3     | Requiere como mínimo Windows Installer 2.0 para que se aplique la revisión. Se produce un error inmediatamente en una revisión con un recuento de palabras de "3" si se usa con una versión Windows Installer anterior a la 2.0. |
| 4     | Requiere como mínimo Windows Installer 3.0 para que se aplique la revisión. Se produce un error en una revisión con un recuento de palabras de "4" si se usa con una Windows installer anterior a la 3.0.             |
| 5     | Requiere como mínimo Windows Installer 3.1 para que se aplique la revisión.                                                                                                               |



 

Esta propiedad de resumen es REQUIRED.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Descripciones de propiedades de resumen](summary-property-descriptions.md)
</dt> </dl>

 

 




