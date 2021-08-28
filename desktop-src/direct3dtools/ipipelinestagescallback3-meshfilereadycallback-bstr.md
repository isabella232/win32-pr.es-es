---
description: Devolución de llamada que notifica al host la información de Mesh escrita por la solicitud asociada.
MS-HAID: vspixengine.IPipeLineStagesCallback3\_MeshFileReadyCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback3::MeshFileReadyCallback (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BD4719A5-AC07-446A-A7CA-5978F869F66E
api_name:
- IPipeLineStagesCallback3.MeshFileReadyCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c695ebad2f8a23757419fe3c6894a91b00cbd2d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625151"
---
# <a name="span-idvspixengineipipelinestagescallback3_meshfilereadycallback_bstrspanipipelinestagescallback3meshfilereadycallback-method"></a><span id="vspixengine.ipipelinestagescallback3_meshfilereadycallback_bstr"></span>IPipeLineStagesCallback3::MeshFileReadyCallback (método)

Devolución de llamada que notifica al host la información de Mesh escrita por la solicitud asociada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MeshFileReadyCallback(
   BSTR meshFilename
);
```

## <a name="parameters"></a>Parámetros

*meshFilename*   
Cadena COM que contiene el nombre de ruta de acceso del archivo donde se escriben los datos de malla.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IPipeLineStagesCallback3**](/windows/desktop/direct3dtools/ipipelinestagescallback3)

 

 
