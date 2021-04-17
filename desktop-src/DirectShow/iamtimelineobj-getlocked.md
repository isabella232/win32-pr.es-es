---
description: El método GetLocked recupera el estado de edición del objeto (bloqueado o desbloqueado).
ms.assetid: ecd258db-36bf-41b6-9bdf-537efcf0a46a
title: 'IAMTimelineObj:: GetLocked (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 472b7dedbdbd879d4fa49fe874fb9178d0ccdee4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680850"
---
# <a name="iamtimelineobjgetlocked-method"></a>IAMTimelineObj:: GetLocked (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetLocked` método recupera el estado de edición del objeto (bloqueado o desbloqueado). Un estado bloqueado indica que el objeto no se debe editar; un estado desbloqueado indica que el objeto se puede editar. La escala de tiempo no aplica el bloqueo. La configuración bloqueada solo existe para la comodidad de la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
 GetLocked(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* 
</dt> <dd>

Recibe el estado de edición del objeto. Si el valor es **true**, el objeto está bloqueado y no se debe editar. Si es **false**, el objeto se desbloquea y se puede editar.

</dd> </dl>

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




