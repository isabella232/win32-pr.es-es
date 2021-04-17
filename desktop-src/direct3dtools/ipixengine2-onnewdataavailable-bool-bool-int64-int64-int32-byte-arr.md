---
description: Solicitudes para indicar que el registro de gráficos tiene nuevos datos dentro de él.
MS-HAID: vspixengine.IPixEngine2\_OnNewDataAvailable\_BOOL\_BOOL\_INT64\_INT64\_INT32\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine2:: OnNewDataAvailable (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B99FC54C-9395-4B14-93D5-B6408D655DC3
api_name:
- IPixEngine2.OnNewDataAvailable
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3de880153eec5b41849167f3a87a3f77f31aeffd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537299"
---
# <a name="span-idvspixengineipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arrspanipixengine2onnewdataavailable-method"></a><span id="vspixengine.ipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arr"></span>IPixEngine2:: OnNewDataAvailable (método)

Solicitudes para indicar que el registro de gráficos tiene nuevos datos dentro de él.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnNewDataAvailable(
   BOOL    fSessionEnd,
   BOOL    fUnloadCurFrame,
   INT64   i64FilePositionStart,
   INT64   i64FilePositionEnd,
   INT32   iObjectTableDataSize,
   BYTE [] count4_pObjectTableData
);
```

## <a name="parameters"></a>Parámetros

*fSessionEnd*   
True si la sesión ha finalizado; de lo contrario, false.

*fUnloadCurFrame*   
No se utiliza.

*i64FilePositionStart*   
La posición del archivo, en bytes, a la que se inician los nuevos datos.

*i64FilePositionEnd*   
Posición del archivo, en bytes, a la que finalizan los nuevos datos.

*iObjectTableDataSize*   
El número de bytes contenidos en count4 \_ pObjectTableData.

*count4 \_ pObjectTableData*   
Búfer que contiene los datos de la tabla de objetos.

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IPixEngine2**](/windows/desktop/direct3dtools/ipixengine2)

 

 
