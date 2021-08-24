---
title: Método IVMDisplay SetDimensions (VPCCOMInterfaces.h)
description: Establece el alto y el ancho de la pantalla de la máquina virtual, en píxeles.
ms.assetid: 8ad5cfc4-59b4-4327-b088-d54adf9c6fda
keywords:
- SetDimensions, método Virtual PC
- Método SetDimensions De PC virtual, interfaz IVMDisplay
- IVMDisplay interface Virtual PC , SetDimensions method
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
ms.openlocfilehash: 5bbf1db342342e9fbb8c0eff2df18f9c2a76443a4d20014bad34934ccecd3dfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473365"
---
# <a name="ivmdisplaysetdimensions-method"></a>IVMDisplay::SetDimensions (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

*displayPixelWidth* \[ En\]
</dt> <dd>

Ancho, en píxeles. El valor debe estar entre los valores de 640 y 2048. Si el valor no es divisible uniformemente por 8, se reducirá al siguiente múltiplo inferior de 8.

</dd> <dt>

*displayPixelHeight* \[ En\]
</dt> <dd>

Alto, en píxeles. El valor debe estar entre los valores de 480 y 1920.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                    | Descripción                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                          | La operación se realizó correctamente.<br/>                                                                                                                                                                         |
| <dl> <dt>**E \_ InvalidarG**</dt> <dt>0x80000003</dt> </dl>                         | El *parámetro displayPixelWidth* no es divisible uniformemente por 8 o el parámetro *displayPixelWidth* o *displayPixelHeight* está fuera de los valores mínimos permitidos (640 x 480) o máximo 2048 x 1920).<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ TIEMPO DE ESPERA \_ 0XA0040202**</dt> <dt></dt> </dl>                     | El cambio de resolución no finaló de forma oportuna.<br/>                                                                                                                                              |
| <dl> <dt>**Máquina virtual \_ E \_ LA MÁQUINA VIRTUAL NO \_ \_ SE**</dt> <dt>0XA0040206</dt> </dl>               | La máquina virtual debe estar en ejecución para esta operación.<br/>                                                                                                                                               |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                    | La máquina virtual no es válida o no se está ejecutando actualmente.<br/>                                                                                                                                         |
| <dl> <dt>**Máquina virtual \_ E \_ NO \_ DISPLAY**</dt> <dt>0xA0040850</dt> </dl>                    | No se puede encontrar una pantalla válida para la máquina virtual.<br/>                                                                                                                                                          |
| <dl> <dt>**Máquina virtual \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL**</dt> <dt>0XA0040505</dt> </dl> | La versión de los componentes de integración instalados en el sistema operativo invitado no admite esta operación.<br/>                                                                                    |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                    | Se produjo un error inesperado.<br/>                                                                                                                                                                     |



 

## <a name="remarks"></a>Comentarios

El tamaño mínimo de la pantalla de la máquina virtual es de 640 x 480 píxeles. El tamaño máximo es 2048 x 1920. Los intentos de establecer el tamaño de presentación en valores fuera de estos límites, o en cualquier ancho que no sea divisible uniformemente por 8, provocarán que se devuelva un error **E \_ INVALIDARG.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMDisplay se define como \_ 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

