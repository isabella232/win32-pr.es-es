---
description: El método GetGroup recupera un grupo especificado.
ms.assetid: 4ff651e5-a3aa-4da9-af23-a3a2bdbf7c5b
title: Método IAMTimeline::GetGroup (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 71bf4aa0dd5d6f338da43d71384ead024fe821d3a639b0021299f6f6deb14be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685195"
---
# <a name="iamtimelinegetgroup-method"></a>IAMTimeline::GetGroup (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetGroup` método recupera un grupo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetGroup(
  [out] IAMTimelineObj **ppGroup,
        long           WhichGroup
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppGroup* \[ out\]
</dt> <dd>

Recibe un puntero a la interfaz [**IAMTimelineObj del**](iamtimelineobj.md) grupo.

</dd> <dt>

*WhichGroup* 
</dt> <dd>

Índice del grupo que se va a recuperar, en función del orden en el que se agregaron los grupos a la escala de tiempo. El primer grupo agregado a la escala de tiempo tiene un índice de 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Si el método se realiza correctamente, la **interfaz IAMTimelineObj** que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando haya terminado de usarlo.

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

[**IamTimeline (interfaz)**](iamtimeline.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




