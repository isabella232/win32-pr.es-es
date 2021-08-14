---
description: Función de devolución de llamada que se usa para notificar al host de errores durante la captura o reproducción.
MS-HAID: vspixengine.IFileIOCallback\_ResultCallback\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFileIOCallback::ResultCallback (Método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E4418A63-47C6-4F12-94FA-0F1B5465FE84
api_name:
- IFileIOCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f1adc4fdc72cd26e317a2d8dc4a82049a2ef6ad99734d5e8bfc631bffdf4df99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981525"
---
# <a name="span-idvspixengineifileiocallback_resultcallback_dwordspanifileiocallbackresultcallback-method"></a><span id="vspixengine.ifileiocallback_resultcallback_dword"></span>IFileIOCallback::ResultCallback (Método)

Función de devolución de llamada que se usa para notificar al host de errores durante la captura o reproducción.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ResultCallback(
   DWORD resultState
);
```

## <a name="parameters"></a>Parámetros

*resultState*   
Indica el tipo de error encontrado.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IFileIOCallback**](/windows/desktop/direct3dtools/ifileiocallback)

 

 
