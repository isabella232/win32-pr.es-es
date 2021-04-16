---
title: Método IVMDisplay SetDimensions (VPCCOMInterfaces. h)
description: Establece el alto y el ancho de la pantalla de la máquina virtual, en píxeles.
ms.assetid: 8ad5cfc4-59b4-4327-b088-d54adf9c6fda
keywords:
- Método SetDimensions Virtual PC
- Método SetDimensions Virtual PC, interfaz IVMDisplay
- Interfaz IVMDisplay Virtual PC, método SetDimensions
topic_type:
- apiref
api_name:
- IVMDisplay.SetDimensions
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4730d73e06074714c8e6ed31fda992259d5c19ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676911"
---
# <a name="ivmdisplaysetdimensions-method"></a>IVMDisplay:: SetDimensions (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Establece el alto y el ancho de la pantalla (VM) de la máquina virtual, en píxeles.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDimensions(
  [in] long displayPixelWidth,
  [in] long displayPixelHeight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*displayPixelWidth* \[ de\]
</dt> <dd>

Ancho, en píxeles. El valor debe estar entre los valores 640 y 2048. Si el valor no es divisible por 8, se reducirá al siguiente múltiplo inferior de 8.

</dd> <dt>

*displayPixelHeight* \[ de\]
</dt> <dd>

Alto, en píxeles. El valor debe estar entre los valores 480 y 1920.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                    | Descripción                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                          | La operación se realizó correctamente.<br/>                                                                                                                                                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                         | El parámetro *displayPixelWidth* no es divisible de forma uniforme por 8 o el parámetro *displayPixelWidth* o *displayPixelHeight* está fuera de los valores mínimo permitido (640x480) o máximo 2048x1920).<br/> |
| <dl> <dt>**Máquina virtual \_ 0xA0040202 \_ agotó el tiempo de \_ espera**</dt> <dt></dt> </dl>                     | El cambio de resolución no finalizó a tiempo.<br/>                                                                                                                                              |
| <dl> <dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt> </dl>               | La máquina virtual debe estar en ejecución para esta operación.<br/>                                                                                                                                               |
| <dl> <dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt> </dl>                    | La máquina virtual no es válida o no se está ejecutando actualmente.<br/>                                                                                                                                         |
| <dl> <dt>**Máquina virtual \_ E \_ no \_ Mostrar**</dt> <dt>0xA0040850</dt> </dl>                    | No se puede encontrar una presentación válida para la máquina virtual.<br/>                                                                                                                                                          |
| <dl> <dt>**Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible**</dt> <dt>0xA0040505</dt> </dl> | La versión de los componentes de integración instalados en el sistema operativo invitado no admite esta operación.<br/>                                                                                    |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                    | Se produjo un error inesperado.<br/>                                                                                                                                                                     |



 

## <a name="remarks"></a>Observaciones

El tamaño mínimo de la pantalla de la máquina virtual es 640 x 480 píxeles. El tamaño máximo es 2048 x 1920. Los intentos de establecer el tamaño de la pantalla en valores fuera de estos límites, o en cualquier ancho que no sea divisible uniformemente por 8, darán lugar a que se devuelva un error de **E \_ INVALIDARG** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay se define como 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

