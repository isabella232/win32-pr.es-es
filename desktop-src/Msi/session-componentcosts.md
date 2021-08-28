---
description: La propiedad ComponentCosts del objeto Session devuelve un objeto RecordList que enumera el espacio en disco por unidad necesario para instalar un componente.
ms.assetid: 9b1355f1-cc99-49d9-8187-07fba4804d1f
title: Propiedad Session.ComponentCosts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCosts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 643996bccd352695651fb55f2ddcb33c0888773f4d99283f646a7fcb498c4074
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629525"
---
# <a name="sessioncomponentcosts-property"></a>Propiedad Session.ComponentCosts

La propiedad ComponentCosts del objeto [**Session**](session-object.md) devuelve un objeto [**RecordList**](recordlist-object.md) que enumera el espacio en disco por unidad necesario para instalar un componente. La interfaz de usuario usa esta información para mostrar el espacio en disco necesario para todas las unidades. Los costos de espacio en disco devueltos se encuentran en múltiplos de 512 bytes.

La propiedad ComponentCosts solo debe usarse [](file-costing.md) después de que el instalador haya completado el costo del archivo y después de [la acción CostFinalize](costfinalize-action.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.ComponentCosts
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

Para obtener el costo total, agregue los costos de todos los componentes más el costo del motor del instalador (Componente = "").

ComponentCosts devuelve un [**objeto RecordList**](recordlist-object.md). Cada registro del objeto RecordList devuelto tiene los siguientes campos:



| Campo | Descripción                                          |
|-------|------------------------------------------------------|
| 1     | Nombre de volumen o unidad                                    |
| 2     | Costo de espacio en disco final en múltiplo de 512 bytes.     |
| 3     | Costo de espacio en disco temporal en múltiplo de 512 bytes. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-00000000046<br/>                                                                                                                                                                             |



 

 




