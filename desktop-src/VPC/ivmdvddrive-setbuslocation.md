---
title: Método IVMDVDDrive SetBusLocation (VPCCOMInterfaces. h)
description: Conecta la unidad de DVD a la ubicación de bus especificada en la máquina virtual.
ms.assetid: 765274b8-91bc-475a-ac4d-994b2425a421
keywords:
- Método SetBusLocation Virtual PC
- Método SetBusLocation Virtual PC, interfaz IVMDVDDrive
- Interfaz IVMDVDDrive Virtual PC, método SetBusLocation
topic_type:
- apiref
api_name:
- IVMDVDDrive.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db6091493a56c020f57300e65328fee0eb65a69e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676767"
---
# <a name="ivmdvddrivesetbuslocation-method"></a>IVMDVDDrive:: SetBusLocation (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Conecta la unidad de DVD a la ubicación de bus especificada en la máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetBusLocation(
  [in] long busNumber,
  [in] long deviceNumber
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*busNumber* \[ de\]
</dt> <dd>

Número de bus al que se va a adjuntar esta unidad. Por ejemplo, en un bus IDE, este número representaría si se usara el número de bus principal o secundario.

</dd> <dt>

*deviceNumber* \[ de\]
</dt> <dd>

Número de dispositivo al que se va a adjuntar esta unidad. Por ejemplo, en un bus IDE, este número representaría si se usara la ubicación del dispositivo principal o secundario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                            | Descripción                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                  | La operación se realizó correctamente.<br/>                                                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                 | La ubicación de bus especificada no es válida.<br/>                                                                                     |
| <dl> <dt>**E \_ ERROR**</dt> <dt>0x80004005</dt> </dl>                       | Se produjo un error inesperado.<br/>                                                                                            |
| <dl> <dt>**Máquina virtual \_ \_Máquina virtual en \_ ejecución \_ o \_ guardada**</dt> <dt>0xA004020B</dt> </dl> | No se puede establecer la ubicación del bus mientras la máquina virtual está en ejecución o en un estado guardado.<br/>                                     |
| <dl> <dt>**VM \_ E \_ bus \_ Loc \_ en \_ uso**</dt> </dl>                                                                      | Otro dispositivo ya está conectado a la ubicación de bus especificada.<br/>                                                            |
| <dl> <dt>**Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida**</dt> <dt></dt> </dl>         | No se pudo inicializar la unidad actual.<br/>                                                                                  |
| <dl> <dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt> </dl>            | No se pudieron escribir los cambios en el archivo de preferencias porque no se pudo determinar la máquina virtual de esta unidad.<br/> |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>            | Se produjo un error inesperado.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive se define como b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

