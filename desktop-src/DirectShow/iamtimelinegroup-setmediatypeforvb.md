---
description: El método SetMediaTypeForVB especifica el tipo de medio de grupo para los clientes de Automation.
ms.assetid: 86f52088-a0dd-40be-98a0-8adc09b264dd
title: Método IAMTimelineGroup::SetMediaTypeForVB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaTypeForVB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ea47e4edcdfc58e38e61a9f92eb5afac0092ab0cb445f6ff73471e1b65b1480b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905045"
---
# <a name="iamtimelinegroupsetmediatypeforvb-method"></a>Método IAMTimelineGroup::SetMediaTypeForVB

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetMediaTypeForVB` método especifica el tipo de medio de grupo para los clientes de Automation.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMediaTypeForVB(
  [in] long Val
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Val* \[ En\]
</dt> <dd>

Valor que especifica el tipo de medio. Establezca el valor en 0 para vídeo o 1 para audio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Este método está pensado para clientes de Automation. Para las aplicaciones de C++, use el [**método IAMTimelineGroup::SetMediaType.**](iamtimelinegroup-setmediatype.md)

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

 

 




