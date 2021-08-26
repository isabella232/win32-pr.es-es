---
description: Finaliza la extensión y completa el registro de gráficos.
MS-HAID: vspixengine.IPixEngine2\_EndExperiment\_BSTR\_IFileIOCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine2::EndExperiment (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0260F337-B279-4FE6-92F3-FCF70C2B8980
api_name:
- IPixEngine2.EndExperiment
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 87d49b1960d43d1d9e2b931b01c89e09ee3cb579
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623481"
---
# <a name="span-idvspixengineipixengine2_endexperiment_bstr_ifileiocallback_ptrspanipixengine2endexperiment-method"></a><span id="vspixengine.ipixengine2_endexperiment_bstr_ifileiocallback_ptr"></span>IPixEngine2::EndExperiment (método)

Finaliza la extensión y completa el registro de gráficos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndExperiment(
   BSTR              logFile,
   IFileIOCallback * pCallback
);
```

## <a name="parameters"></a>Parámetros

*Logfile*   
Cadena COM que contiene el nombre del registro de gráficos.

*pCallback*   
Dirección de una devolución de llamada usada para indicar que se ha finalizado la extensión.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IPixEngine2**](/windows/desktop/direct3dtools/ipixengine2)

 

 
