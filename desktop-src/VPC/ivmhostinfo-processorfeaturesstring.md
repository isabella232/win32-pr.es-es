---
title: Propiedad IVMHostInfo ProcessorFeaturesString (VPCCOMInterfaces.h)
description: Recupera las características de lista admitidas por el procesador host.
ms.assetid: 036c6376-0e9b-46fa-90f4-a40c71c5cf23
keywords:
- ProcessorFeaturesString, propiedad Virtual PC
- Propiedad ProcessorFeaturesString virtual PC , interfaz IVMHostInfo
- Interfaz IVMHostInfo pc virtual, propiedad ProcessorFeaturesString
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorFeaturesString
- IVMHostInfo.get_ProcessorFeaturesString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1040702df250c906bb32af5068a340c37a9ba3faabee3af17d8397bfdc8059e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998895"
---
# <a name="ivmhostinfoprocessorfeaturesstring-property"></a>Propiedad IVMHostInfo::P rocessorFeaturesString

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera las características de lista admitidas por el procesador host.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ProcessorFeaturesString(
  [out, retval] BSTR *featuresString
);
```



## <a name="property-value"></a>Valor de propiedad

Una lista delimitada por comas de características. Un ejemplo sería "MMX, SSE, SSE2, x86-64".



| Value                                                                                 | Significado                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>"AMD-V"</dt> </dl>    | Admite las extensiones de virtualización de AMD.<br/>              |
| <dl> <dt>"Intel VT"</dt> </dl> | Admite las extensiones intel virtualization technology.<br/> |
| <dl> <dt>"HAVD"</dt> </dl>     | La virtualización asistida por hardware está deshabilitada.<br/>            |
| <dl> <dt>"HAVE"</dt> </dl>     | La virtualización asistida por hardware está habilitada.<br/>             |
| <dl> <dt>"MMX"</dt> </dl>      | Admite las extensiones MMX.<br/>                             |
| <dl> <dt>"SSE"</dt> </dl>      | Admite las extensiones SIMD de streaming.<br/>                  |
| <dl> <dt>"SSE2"</dt> </dl>     | Admite las extensiones SIMD de streaming 2.<br/>                |
| <dl> <dt>"SSE3"</dt> </dl>     | Admite las extensiones SIMD de streaming 3.<br/>                |
| <dl> <dt>"TXTE"</dt> </dl>     | Admite las extensiones de tecnología de ejecución de confianza.<br/>    |
| <dl> <dt>"x86-64"</dt> </dl>   | Admite extensiones x86-64.<br/>                              |



 

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHostInfo se define como \_ 5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

