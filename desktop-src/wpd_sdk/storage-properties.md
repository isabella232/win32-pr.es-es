---
description: Windows Dispositivos portátiles admite las siguientes propiedades de almacenamiento.
ms.assetid: 234078c3-e703-41f3-9b18-ae61d8a36784
title: Storage Propiedades (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Storage
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 0dbf88d02e59cca59e4bb3ee14ffd90c1741478f8b6a90ea296087388b9bb099
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806515"
---
# <a name="storage-properties"></a>Propiedades de almacenamiento

Windows Dispositivos portátiles admite las siguientes propiedades de almacenamiento.



| Propiedad                                   | VarType        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CAPACIDAD DE \_ ALMACENAMIENTO DE \_ WPD**                 | **VT \_ UI8**    | Capacidad de almacenamiento total, en bytes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **CAPACIDAD DE \_ ALMACENAMIENTO \_ WPD \_ EN \_ OBJETOS**    | **VT \_ UI8**    | Indica la capacidad de almacenamiento total en objetos ; por ejemplo, las ranuras disponibles en una tarjeta SIM.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **DESCRIPCIÓN DE \_ ALMACENAMIENTO DE \_ WPD**              | **VT \_ LPWSTR** | Descripción legible del almacenamiento.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **TIPO DE \_ SISTEMA DE ARCHIVOS DE ALMACENAMIENTO \_ \_ \_ WPD**       | **VT \_ LPWSTR** | Una descripción de cadena del sistema de archivos utilizado por el almacenamiento, por ejemplo, "FAT32", "NTFS", "Contoso File System", y así sucesivamente.                                                                                                                                                                                                                                                                                                                                                                                                         |
| **ESPACIO LIBRE \_ DE ALMACENAMIENTO \_ WPD EN \_ \_ \_ BYTES**   | **VT \_ UI8**    | Espacio de almacenamiento disponible, en bytes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **ESPACIO LIBRE \_ DE ALMACENAMIENTO \_ WPD EN \_ \_ \_ OBJETOS** | **VT \_ UI8**    | Número de objetos adicionales que se pueden escribir en el dispositivo. Por ejemplo, si un dispositivo solo permite un único objeto, sería cero si el objeto ya existía.                                                                                                                                                                                                                                                                                                                                                          |
| **NÚMERO DE \_ SERIE DE ALMACENAMIENTO DE \_ \_ WPD**           | **VT \_ LPWSTR** | Número de serie específico del proveedor para el almacenamiento.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **TAMAÑO MÁXIMO \_ DE OBJETO \_ DE ALMACENAMIENTO DE \_ WPD \_**        | **VT \_ UI8**    | Especifica el tamaño máximo de un único objeto, en bytes, que se puede colocar en este almacenamiento.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **TIPO DE \_ ALMACENAMIENTO \_ WPD**                     | **VT \_ UI4**    | Describe el tipo físico de un medio de almacenamiento de memoria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **FUNCIONALIDAD DE \_ ACCESO \_ AL ALMACENAMIENTO \_ WPD**       | **VT \_ UI4**    | Identifica cualquier protección contra escritura que afecte globalmente a este almacenamiento. Esto tiene prioridad sobre el acceso especificado en objetos individuales. Los valores posibles son de la **enumeración \_ WPD STORAGE \_ ACCESS \_ CAPABILITY \_ VALUES** definida en PortableDevice.h. Por ejemplo, si **WPD \_ STORAGE \_ TYPE** es ROM (es decir, **WPD \_ STORAGE TYPE \_ FIXED \_ \_ ROM** o **WPD STORAGE TYPE \_ \_ \_ REMOVABLE \_ ROM),** el valor DE **WPD \_ STORAGE ACCESS \_ \_ CAPABILITY** debe ser **WPD STORAGE ACCESS \_ \_ \_ CAPABILITY READ ONLY \_ WITHOUT OBJECT \_ \_ \_ \_ DELETION**. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




