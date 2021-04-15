---
title: IAMWMBufferPass SetNotify, método
description: Las aplicaciones usan el método SetNotify para proporcionar el filtro WM ASF Writer o el lector ASF de WM con un puntero a la interfaz IAMWMBufferPassCallback de la aplicación.
ms.assetid: b0fff344-a20c-4cfc-828b-c6fc49d990ea
keywords:
- Método SetNotify formato de Windows Media
- Método SetNotify formato de Windows Media, interfaz IAMWMBufferPass
- Interfaz IAMWMBufferPass formato de Windows Media, método SetNotify
topic_type:
- apiref
api_name:
- IAMWMBufferPass.SetNotify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9739952792fcfa49da1b5656db513c3af41a419c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421247"
---
# <a name="iamwmbufferpasssetnotify-method"></a>IAMWMBufferPass:: SetNotify (método)

Las aplicaciones usan el método **SetNotify** para proporcionar el filtro WM ASF Writer o el [lector ASF de WM](wm-asf-reader-filter.md) con un puntero a la interfaz [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) de la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetNotify(
  [in] IAMWMBufferPassCallback *pCallback
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCallback* \[ de\]
</dt> <dd>

Puntero a la interfaz **IAMWMBufferPassCallback** de la aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve S \_ correcto. Si se produce un error, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Llame a este método antes de colocar el gráfico de filtro en el estado de ejecución.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)
</dt> </dl>

 

 