---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de almacenamiento.
ms.assetid: 234078c3-e703-41f3-9b18-ae61d8a36784
title: Propiedades de almacenamiento (PortableDevice. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708671"
---
# <a name="storage-properties"></a>Propiedades de almacenamiento

Los dispositivos portátiles de Windows admiten las siguientes propiedades de almacenamiento.



| Propiedad                                   | VarType        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_capacidad de almacenamiento de WPD \_**                 | **VT \_ UI8**    | La capacidad total de almacenamiento, en bytes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **\_ \_ capacidad de almacenamiento \_ de WPD en \_ objetos**    | **VT \_ UI8**    | Indica la capacidad total de almacenamiento en objetos; por ejemplo, las ranuras disponibles en una tarjeta SIM.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **\_Descripción del almacenamiento de WPD \_**              | **VT \_ LPWStr** | Una descripción inteligible del almacenamiento.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **\_tipo de \_ sistema de archivos de almacenamiento de WPD \_ \_**       | **VT \_ LPWStr** | Una descripción de cadena del sistema de archivos que usa el almacenamiento, por ejemplo, "FAT32", "NTFS", "sistema de archivos de Contoso", etc.                                                                                                                                                                                                                                                                                                                                                                                                         |
| **\_ \_ espacio libre en el almacenamiento \_ de WPD \_ en \_ bytes**   | **VT \_ UI8**    | Espacio de almacenamiento disponible, en bytes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **\_ \_ espacio libre en el almacenamiento \_ de WPD \_ en \_ objetos** | **VT \_ UI8**    | El número de objetos adicionales que se pueden escribir en el dispositivo. Por ejemplo, si un dispositivo solo permite un único objeto, es cero si el objeto ya existía.                                                                                                                                                                                                                                                                                                                                                          |
| **\_número de \_ serie de almacenamiento de WPD \_**           | **VT \_ LPWStr** | Un número de serie específico del proveedor para el almacenamiento.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **\_ \_ tamaño máximo de \_ objeto de almacenamiento de \_ WPD**        | **VT \_ UI8**    | Especifica el tamaño máximo de un solo objeto, en bytes, que se puede colocar en este almacenamiento.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **\_tipo de almacenamiento de WPD \_**                     | **VT \_ UI4**    | Describe el tipo físico de un medio de almacenamiento de memoria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **\_funcionalidad de \_ acceso al almacenamiento de WPD \_**       | **VT \_ UI4**    | Identifica cualquier protección contra escritura que afecte globalmente a este almacenamiento. Esto tiene prioridad sobre el acceso especificado en objetos individuales. Los valores posibles proceden de la enumeración de **\_ valores de \_ \_ capacidad \_ de acceso al almacenamiento de WPD** definidas en PortableDevice. h. Por ejemplo, si **el \_ \_ tipo de almacenamiento de WPD** es ROM (es decir, el tipo de almacenamiento de la **\_ \_ \_ \_ ROM** o el tipo de almacenamiento WPD **\_ \_ \_ extraíble \_**), el valor de **\_ \_ \_ capacidad de acceso al almacenamiento** de WPD debe ser la **función de \_ acceso al almacenamiento de WPD \_ \_ \_ leer \_ solo \_ sin \_ \_ eliminar objetos**. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




