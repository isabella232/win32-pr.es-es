---
title: Método IAMWMBufferPass SetNotify
description: Las aplicaciones usan el método SetNotify para proporcionar el filtro WM ASF Writer o WM ASF Reader con un puntero a la interfaz IAMWMBufferPassCallback de la aplicación.
ms.assetid: b0fff344-a20c-4cfc-828b-c6fc49d990ea
keywords:
- SetNotify method windows Media Format
- Método SetNotify windows Media Format , interfaz IAMWMBufferPass
- IamWMBufferPass interface windows Media Format , SetNotify (método)
topic_type:
- apiref
api_name:
- IAMWMBufferPass.SetNotify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47e189a2654ed4c760fdfcd6ced5506cc90d5e7cc989a7f79979e6d95b0bbfb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847611"
---
# <a name="iamwmbufferpasssetnotify-method"></a>IAMWMBufferPass::SetNotify (método)

Las aplicaciones usan el método **SetNotify** para proporcionar el filtro WM ASF Writer o [WM ASF Reader](wm-asf-reader-filter.md) con un puntero a la interfaz [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) de la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetNotify(
  [in] IAMWMBufferPassCallback *pCallback
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCallback* \[ En\]
</dt> <dd>

Puntero a la interfaz **IAMWMBufferPassCallback de la** aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve S \_ OK. Si se produce un error, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Llame a este método antes de colocar el gráfico de filtro en el estado de ejecución.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IAMWMBufferPass (interfaz)**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)
</dt> </dl>

 

 