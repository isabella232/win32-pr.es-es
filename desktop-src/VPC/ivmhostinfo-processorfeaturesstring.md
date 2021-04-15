---
title: Propiedad IVMHostInfo ProcessorFeaturesString (VPCCOMInterfaces. h)
description: Recupera las características de lista que admite el procesador del host.
ms.assetid: 036c6376-0e9b-46fa-90f4-a40c71c5cf23
keywords:
- Propiedad ProcessorFeaturesString Virtual PC
- Propiedad ProcessorFeaturesString Virtual PC, interfaz IVMHostInfo
- Interfaz IVMHostInfo Virtual PC, propiedad ProcessorFeaturesString
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
ms.openlocfilehash: 118aaa2eabe7ddb2fd608892775a17eac6a77d16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676549"
---
# <a name="ivmhostinfoprocessorfeaturesstring-property"></a>IVMHostInfo::P propiedad rocessorFeaturesString

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera las características de lista que admite el procesador del host.

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
| <dl> <dt>"AMD-V"</dt> </dl>    | Es compatible con las extensiones de virtualización de AMD.<br/>              |
| <dl> <dt>"Intel VT"</dt> </dl> | Es compatible con las extensiones de tecnología de virtualización de Intel.<br/> |
| <dl> <dt>"HAVD"</dt> </dl>     | La virtualización asistida por hardware está deshabilitada.<br/>            |
| <dl> <dt>Has</dt> </dl>     | La virtualización asistida por hardware está habilitada.<br/>             |
| <dl> <dt>MMX</dt> </dl>      | Es compatible con las extensiones MMX.<br/>                             |
| <dl> <dt>SSE</dt> </dl>      | Admite las extensiones SIMD de streaming.<br/>                  |
| <dl> <dt>DICHAS</dt> </dl>     | Admite las extensiones SIMD de streaming 2.<br/>                |
| <dl> <dt>SSE3</dt> </dl>     | Admite las extensiones SIMD de streaming 3.<br/>                |
| <dl> <dt>"TXTE"</dt> </dl>     | Es compatible con las extensiones de tecnología de ejecución de confianza.<br/>    |
| <dl> <dt>"x86-64"</dt> </dl>   | Admite extensiones x86-64.<br/>                              |



 

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **null**.<br/>        |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo se define como 5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

