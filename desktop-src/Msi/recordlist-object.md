---
description: El objeto RecordList es una colección de objetos record. Debe comprobar que el objeto RecordList existe y que no está vacío antes de hacer referencia a sus propiedades.
ms.assetid: 7f5ac153-8da1-4dc8-9bb7-defd4e821142
title: Objeto RecordList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b3f09887333d8ddbf83de4bea2b2e654411883e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680758"
---
# <a name="recordlist-object"></a>Objeto RecordList

El objeto **RecordList** es una colección de objetos [**Record**](record-object.md) . Debe comprobar que el objeto **RecordList** existe y que no está vacío antes de hacer referencia a sus propiedades.

## <a name="members"></a>Miembros

El objeto **RecordList** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **RecordList** tiene estas propiedades.



| Propiedad                                     | Descripción                                                          |
|:---------------------------------------------|:---------------------------------------------------------------------|
| [**Contabiliza**](recordlist-count.md)<br/> | Devuelve el número de elementos del objeto **RecordList** .<br/> |
| [**Elemento**](recordlist-item.md)<br/>   | Devuelve un registro de una colección de objetos **RecordList** .<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecordList se define como 000C1096-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Record**](record-object.md)
</dt> <dt>

[Ejemplos de scripting Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




