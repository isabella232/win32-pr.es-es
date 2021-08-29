---
title: Propiedad VideoMode de IVMDisplay (VPCCOMInterfaces.h)
description: Recupera el modo de vídeo actual.
ms.assetid: e5a090c2-f7e6-4b85-8729-64d2ff68fcf3
keywords:
- VideoMode, propiedad Virtual PC
- Propiedad VideoMode Virtual PC, interfaz IVMDisplay
- Interfaz IVMDisplay Pc virtual, propiedad VideoMode
topic_type:
- apiref
api_name:
- IVMDisplay.VideoMode
- IVMDisplay.get_VideoMode
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48ae239671bb3b3029635830c4b549479346e3c98ce819b809b00f9bddfeb8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136868"
---
# <a name="ivmdisplayvideomode-property"></a>IVMDisplay::VideoMode, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el modo de vídeo actual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_VideoMode(
  [out, retval] VMDisplayVideoMode *videoMode
);
```



## <a name="property-value"></a>Valor de propiedad

Modo de vídeo actual del sistema operativo invitado. Para obtener una lista de valores, [**vea VMDisplayVideoMode**](vmdisplayvideomode.md).

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                         | Significado                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                            | La operación se realizó correctamente.<br/>                                 |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>              | El parámetro es **NULL.**<br/>                                    |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl> | La máquina virtual debe estar en ejecución para esta operación.<br/>       |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>      | La máquina virtual no es válida o no se está ejecutando actualmente.<br/> |
| <dl> <dt>Máquina virtual \_ E \_ NO \_ DISPLAY</dt> <dt>0xA0040850</dt> </dl>      | No se puede encontrar una pantalla válida para la máquina virtual.<br/>     |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>      | Se produjo un error inesperado.<br/>                             |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMDisplay se define como \_ 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

