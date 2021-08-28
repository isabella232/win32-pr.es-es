---
description: Devolución de llamada usada para notificar al host que se ha actualizado un objeto.
MS-HAID: vspixengine.IUpdateObjectCallback\_UpdateComplete\_UINT\_HRESULT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IUpdateObjectCallback::UpdateComplete (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7F54DDEC-E595-4615-B9B7-B1213A58B362
api_name:
- IUpdateObjectCallback.UpdateComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e9ab83b3edf4e817e4e697a5bb72bf41f66508c2
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631853"
---
# <a name="span-idvspixengineiupdateobjectcallback_updatecomplete_uint_hresultspaniupdateobjectcallbackupdatecomplete-method"></a><span id="vspixengine.iupdateobjectcallback_updatecomplete_uint_hresult"></span>IUpdateObjectCallback::UpdateComplete (método)

Devolución de llamada usada para notificar al host que se ha actualizado un objeto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UpdateComplete(
   UINT    objectAddress,
   HRESULT result
);
```

## <a name="parameters"></a>Parámetros

*objectAddress*   
Identificador del objeto que se actualizó.

*Resultado*   
Indica si la actualización se ha actualizado correctamente o no.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IUpdateObjectCallback**](/windows/desktop/direct3dtools/iupdateobjectcallback)

 

 
