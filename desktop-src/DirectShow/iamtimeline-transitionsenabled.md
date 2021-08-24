---
description: El método TransitionsEnabled determina si las transiciones están habilitadas.
ms.assetid: c961d8d7-4509-444b-a49f-6ab79fc31f7e
title: Método IAMTimeline::TransitionsEnabled (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.TransitionsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 36d22fa1c19c6a90faa033e6a8ccf100b5042cd2aeeabf9b012ee42f13cd57da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119316475"
---
# <a name="iamtimelinetransitionsenabled-method"></a>IamTimeline::TransitionsEnabled (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El **método TransitionsEnabled** determina si las transiciones están habilitadas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT TransitionsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pfEnabled* 
</dt> <dd>

Recibe un valor booleano. Si **es TRUE,** las transiciones están habilitadas. De lo contrario, las transiciones están deshabilitadas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

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

[**IamTimeline (interfaz)**](iamtimeline.md)
</dt> <dt>

[**IAMTimeline::EnableTransitions**](iamtimeline-enabletransitions.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




