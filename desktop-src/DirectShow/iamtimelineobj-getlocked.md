---
description: El método GetLocked recupera el estado de edición del objeto (bloqueado o desbloqueado).
ms.assetid: ecd258db-36bf-41b6-9bdf-537efcf0a46a
title: Método IAMTimelineObj::GetLocked (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891988"
---
# <a name="iamtimelineobjgetlocked-method"></a>IamTimelineObj::GetLocked (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetLocked` método recupera el estado de edición del objeto (bloqueado o desbloqueado). Un estado bloqueado indica que no se debe editar el objeto; un estado desbloqueado indica que el objeto se puede editar. La escala de tiempo no aplica el bloqueo. La configuración bloqueada solo existe para la comodidad de la aplicación.

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

Recibe el estado de edición del objeto. Si el valor es **TRUE**, el objeto está bloqueado y no se debe editar. Si **es FALSE,** el objeto se desbloquea y se puede editar.

</dd> </dl>

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IamTimelineObj (interfaz)**](iamtimelineobj.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




