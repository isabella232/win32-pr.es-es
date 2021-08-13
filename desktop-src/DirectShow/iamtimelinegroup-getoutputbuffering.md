---
description: El método GetOutputBuffering recupera el número de fotogramas representados de antemano durante la versión preliminar.
ms.assetid: 93cb8d18-f1b7-48f9-af41-97f010304b05
title: Método IAMTimelineGroup::GetOutputBuffering (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 52917e798dcc71526f225fbca01038ee11c36c3c65fa1cebda88883ad2ae530e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428495"
---
# <a name="iamtimelinegroupgetoutputbuffering-method"></a>IamTimelineGroup::GetOutputBuffering (método)

> [!Note]  
> \[En desuso. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetOutputBuffering` método recupera el número de fotogramas representados de antemano durante la versión preliminar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetOutputBuffering(
  [out] int *pnBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pnBuffer* \[ out\]
</dt> <dd>

Recibe el número de fotogramas almacenados en búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IamTimelineGroup (interfaz)**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




