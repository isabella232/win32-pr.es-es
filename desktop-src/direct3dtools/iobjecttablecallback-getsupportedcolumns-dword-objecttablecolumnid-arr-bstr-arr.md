---
description: Obtiene información sobre qué columnas (tipos de datos de objeto) son compatibles con la tabla de objetos.
MS-HAID: vspixengine.IObjectTableCallback\_GetSupportedColumns\_DWORD\_ObjectTableColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IObjectTableCallback::GetSupportedColumns (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 148AB80D-9833-4B57-9F34-CEDFFF8E905A
api_name:
- IObjectTableCallback.GetSupportedColumns
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c55c2e6f5ef304b031565148359bf96adeea248d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631383"
---
# <a name="span-idvspixengineiobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arrspaniobjecttablecallbackgetsupportedcolumns-method"></a><span id="vspixengine.iobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arr"></span>IObjectTableCallback::GetSupportedColumns (método)

Obtiene información sobre qué columnas (tipos de datos de objeto) son compatibles con la tabla de objetos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSupportedColumns(
   DWORD                  numColumns,
   ObjectTableColumnID [] count0_pIDs,
   BSTR []                count0_pBstrNames
);
```

## <a name="parameters"></a>Parámetros

*numColumns*   
Número de columnas admitidas por la tabla de objetos.

*count0_pIDs*   
Los id. de cada columna admitidos por la tabla de objetos.

*count0_pBstrNames*   
Los nombres de cada columna, como una cadena COM, admitidos por la tabla de objetos.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IObjectTableCallback**](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
