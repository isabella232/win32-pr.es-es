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
ms.openlocfilehash: 404b45a6fe5193a0550b3ecc11feeae264125110
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360918"
---
# <a name="storage-properties"></a>Propiedades de almacenamiento

Windows Dispositivos portátiles admite las siguientes propiedades de almacenamiento.



| Propiedad.                                   | VarType        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CAPACIDAD DE \_ ALMACENAMIENTO DE \_ WPD**                 | **VT \_ UI8**    | Capacidad total de almacenamiento, en bytes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **CAPACIDAD DE ALMACENAMIENTO DE WPD \_ \_ EN \_ \_ OBJETOS**    | **VT \_ UI8**    | Indica la capacidad de almacenamiento total en objetos ; por ejemplo, las ranuras disponibles en una tarjeta SIM.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **DESCRIPCIÓN DEL \_ ALMACENAMIENTO DE \_ WPD**              | **VT \_ LPWSTR** | Descripción legible del almacenamiento.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **TIPO DE \_ SISTEMA DE ARCHIVOS DE ALMACENAMIENTO \_ \_ \_ WPD**       | **VT \_ LPWSTR** | Una descripción de cadena del sistema de archivos utilizado por el almacenamiento, por ejemplo, "FAT32", "NTFS", "Contoso File System", y así sucesivamente.                                                                                                                                                                                                                                                                                                                                                                                                         |
| **ESPACIO LIBRE \_ DE ALMACENAMIENTO \_ WPD EN \_ \_ \_ BYTES**   | **VT \_ UI8**    | Espacio de almacenamiento disponible, en bytes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **ESPACIO LIBRE DE ALMACENAMIENTO DE WPD \_ \_ EN \_ \_ \_ OBJETOS** | **VT \_ UI8**    | Número de objetos adicionales que se pueden escribir en el dispositivo. Por ejemplo, si un dispositivo solo permite un único objeto, este sería cero si el objeto ya existía.                                                                                                                                                                                                                                                                                                                                                          |
| **NÚMERO DE SERIE \_ DE ALMACENAMIENTO \_ DE \_ WPD**           | **VT \_ LPWSTR** | Número de serie específico del proveedor para el almacenamiento.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **TAMAÑO MÁXIMO \_ DE OBJETO DE ALMACENAMIENTO DE \_ \_ \_ WPD**        | **VT \_ UI8**    | Especifica el tamaño máximo de un único objeto, en bytes, que se puede colocar en este almacenamiento.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **TIPO DE \_ ALMACENAMIENTO \_ WPD**                     | **VT \_ UI4**    | Describe el tipo físico de un medio de almacenamiento de memoria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **FUNCIONALIDAD DE \_ ACCESO AL ALMACENAMIENTO DE \_ \_ WPD**       | **VT \_ UI4**    | Identifica cualquier protección de escritura que afecte globalmente a este almacenamiento. Esto tiene prioridad sobre el acceso especificado en objetos individuales. Los valores posibles son de la **enumeración \_ WPD STORAGE \_ ACCESS \_ CAPABILITY \_ VALUES** definida en PortableDevice.h. Por ejemplo, si WPD STORAGE TYPE es ROM (es decir, WPD STORAGE **\_ \_ TYPE** **\_ FIXED \_ \_ \_ ROM** o **WPD STORAGE TYPE \_ \_ \_ REMOVABLE \_ ROM),** el valor DE CAPACIDAD DE ACCESO DE ALMACENAMIENTO DE **WPD \_ \_ \_** debe ser **WPD \_ STORAGE ACCESS \_ \_ CAPABILITY READ ONLY WITHOUT \_ \_ OBJECT \_ \_ \_ DELETION**. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




