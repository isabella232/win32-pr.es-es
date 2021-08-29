---
description: Devolución de llamada que notifica al host el progreso de una solicitud asociada.
MS-HAID: vspixengine.IPixProgressCallback\_Progress\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixProgressCallback::P rogress (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BE74599B-C98F-4BDB-ACDF-641F77A35EEB
api_name:
- IPixProgressCallback.Progress
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: fbdc28d4ef248b905f39e03e199a08a30b5f92cf
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626820"
---
# <a name="span-idvspixengineipixprogresscallback_progress_dword_dwordspanipixprogresscallbackprogress-method"></a><span id="vspixengine.ipixprogresscallback_progress_dword_dword"></span>IPixProgressCallback::P rogress (método)

Devolución de llamada que notifica al host el progreso de una solicitud asociada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Progress(
   DWORD current,
   DWORD maxSize
);
```

## <a name="parameters"></a>Parámetros

*Actual*   
Parte de una solicitud completada, como recuento del número de pasos completados.

*Maxsize*   
Número total de pasos para completar la solicitud.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IPixProgressCallback**](/windows/desktop/direct3dtools/ipixprogresscallback)

 

 
