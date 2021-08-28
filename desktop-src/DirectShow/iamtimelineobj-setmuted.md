---
description: El método SetMuted establece el estado muted del objeto. Un objeto muted no se representa, pero permanece en la escala de tiempo.
ms.assetid: 5dcd8533-8e58-4553-ac01-928723485f5d
title: Método IAMTimelineObj::SetMuted (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c561dad9435d972b24a899a9dd7aa65207555b3373fc2930438328aa17568fd1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633885"
---
# <a name="iamtimelineobjsetmuted-method"></a>IamTimelineObj::SetMuted (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetMuted` método establece el estado muted del objeto. Un objeto muted no se representa, pero permanece en la escala de tiempo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMuted(
   BOOL newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* 
</dt> <dd>

Marca que especifica el estado muted. Si **es TRUE,** el objeto y todos sus secundarios están mutados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Muting an object also mutes any children contained in the object. Por ejemplo, si se silencia una pista, las transiciones, los orígenes y los efectos de esa pista también se silencian. Una vez que el objeto ya no está mutado, sus secundarios vuelven a su estado anterior, que podría ser muted o unmuted.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IamTimelineObj (interfaz)**](iamtimelineobj.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




