---
description: La propiedad ComponentQualifiers es una propiedad de solo lectura que devuelve un objeto StringList que enumera el conjunto de calificadores registrados para el componente especificado.
ms.assetid: 49b16c9a-ce84-42ff-af1d-f4ecf7dbe23a
title: Installer.ComponentQualifiers, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentQualifiers
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e6f58850974eaa2021578f0d56015ea0ef6d9e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171713"
---
# <a name="installercomponentqualifiers-property"></a>Installer.ComponentQualifiers, propiedad

La **propiedad ComponentQualifiers** es una propiedad de solo lectura que devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de calificadores registrados para el componente especificado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.ComponentQualifiers
```



## <a name="property-value"></a>Valor de propiedad

GUID de cadena que representa la categoría del [componente](publishcomponent-table.md).

## <a name="remarks"></a>Observaciones

Para enumerar calificadores, la aplicación recorre en iteración el [**objeto StringList**](stringlist-object.md) mediante una construcción For Each. Dado que los calificadores no están ordenados, cualquier nuevo calificador tiene un índice arbitrario, lo que significa que la función puede devolver calificadores en cualquier orden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> </dl>

 

 




