---
description: Función de devolución de llamada que se usa para notificar al host de información acerca de los archivos de código fuente asociados a la pila de llamadas.
MS-HAID: vspixengine.ISourceFileInfoCallback\_ResultCallback\_DWORD\_SourceFileInfo\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ISourceFileInfoCallback:: ResultCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AB3249FF-DA67-4902-B75D-4EC3D0F25EE7
api_name:
- ISourceFileInfoCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a60122615cf15e9ed39ae7809e574c4d3d0c1146
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152676"
---
# <a name="span-idvspixengineisourcefileinfocallback_resultcallback_dword_sourcefileinfo_arrspanisourcefileinfocallbackresultcallback-method"></a><span id="vspixengine.isourcefileinfocallback_resultcallback_dword_sourcefileinfo_arr"></span>ISourceFileInfoCallback:: ResultCallback (método)

Función de devolución de llamada que se usa para notificar al host de información acerca de los archivos de código fuente asociados a la pila de llamadas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ResultCallback(
   DWORD             count,
   SourceFileInfo [] count0_sourceFileInfoBuffer
);
```

## <a name="parameters"></a>Parámetros

*contabiliza*   
Número de archivos de código fuente devueltos.

*count0 \_ sourceFileInfoBuffer*   
Archivos de código fuente.

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**ISourceFileInfoCallback**](/windows/desktop/direct3dtools/isourcefileinfocallback)

 

 
