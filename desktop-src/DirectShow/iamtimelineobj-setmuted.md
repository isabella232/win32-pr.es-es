---
description: El método SetMuted establece el estado silenciado del objeto. Un objeto silenciado no se representa, pero permanece en la escala de tiempo.
ms.assetid: 5dcd8533-8e58-4553-ac01-928723485f5d
title: 'IAMTimelineObj:: SetMuted (método) (QEDIT. h)'
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
ms.openlocfilehash: ac3f5b798ef56251fa64b55a92ae1e94e2fd61b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680727"
---
# <a name="iamtimelineobjsetmuted-method"></a>IAMTimelineObj:: SetMuted (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetMuted` método establece el estado silenciado del objeto. Un objeto silenciado no se representa, pero permanece en la escala de tiempo.

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

Marca que especifica el estado silenciado. Si **es true**, se silencia el objeto y todos sus elementos secundarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Silenciar un objeto también silencia los elementos secundarios contenidos en el objeto. Por ejemplo, si silencia una pista, las transiciones, los orígenes y los efectos de esa pista también se silencian. Una vez que el objeto deja de estar silenciado, sus elementos secundarios se revierten a su estado anterior, lo que podría estar silenciado o desactivado.

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

 

 




