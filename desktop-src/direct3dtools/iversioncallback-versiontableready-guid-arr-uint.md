---
description: Función de devolución de llamada que se usa para notificar al host de qué interfaces se admiten.
MS-HAID: vspixengine.IVersionCallback\_VersionTableReady\_GUID\_arr\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IVersionCallback::VersionTableReady (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 58D5E6B4-2CF8-4C13-9A62-93418D46CBCF
api_name:
- IVersionCallback.VersionTableReady
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 680a9db6fe72dcf11dc6ecb13cf64fede9cf375e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626541"
---
# <a name="span-idvspixengineiversioncallback_versiontableready_guid_arr_uintspaniversioncallbackversiontableready-method"></a><span id="vspixengine.iversioncallback_versiontableready_guid_arr_uint"></span>IVersionCallback::VersionTableReady (método)

Función de devolución de llamada que se usa para notificar al host de qué interfaces se admiten.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT VersionTableReady(
   GUID [] count1_interfaceIds,
   UINT    count
);
```

## <a name="parameters"></a>Parámetros

*count1 \_ interfaceIds*   
Matriz que contiene los GUID de los ID de interfaz admitidos.

*Contar*   
Número de GUID pasados en \_ interfaceIds count1.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IVersionCallback**](/windows/desktop/direct3dtools/iversioncallback)

 

 
