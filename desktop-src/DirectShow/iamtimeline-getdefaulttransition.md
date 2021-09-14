---
description: El método GetDefaultTransition recupera la transición predeterminada. Si el motor de representación no puede representar una transición, sustituye la transición predeterminada.
ms.assetid: 3fe5d984-480b-4b35-970f-2f571e0fde7d
title: Método IAMTimeline::GetDefaultTransition (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultTransition
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f594c0c0be10f93d0e90997df53074a9e69aec6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062321"
---
# <a name="iamtimelinegetdefaulttransition-method"></a>IamTimeline::GetDefaultTransition (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetDefaultTransition` método recupera la transición predeterminada. Si el motor de representación no puede representar una transición, sustituye la transición predeterminada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDefaultTransition(
   GUID *pGuid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pGuid* 
</dt> <dd>

Recibe el GUID de la transición predeterminada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IAMTimeline (interfaz)**](iamtimeline.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




