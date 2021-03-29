---
title: Propiedad ancho IVMDisplay (VPCCOMInterfaces. h)
description: Ancho de la pantalla de la máquina virtual, en píxeles.
ms.assetid: a0062d75-dbb3-41ff-8112-87c1a31b088e
keywords:
- Propiedad width de Virtual PC
- Propiedad Width Virtual PC, interfaz IVMDisplay
- Interfaz IVMDisplay Virtual PC, propiedad width
topic_type:
- apiref
api_name:
- IVMDisplay.Width
- IVMDisplay.get_Width
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b6fe7d329498b0f1ffc36304311f733cd990c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535188"
---
# <a name="ivmdisplaywidth-property"></a>IVMDisplay:: width (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el ancho de la pantalla (VM) de la máquina virtual, en píxeles.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Width(
  [out, retval] long *displayPixelWidth
);
```



## <a name="property-value"></a>Valor de propiedad

Ancho, en píxeles.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                         | Significado                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                            | La operación se realizó correctamente.<br/>                                 |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>              | El parámetro es **null**.<br/>                                    |
| <dl> <dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt> </dl> | La máquina virtual debe estar en ejecución para esta operación.<br/>       |
| <dl> <dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt> </dl>      | La máquina virtual no es válida o no se está ejecutando actualmente.<br/> |
| <dl> <dt>Máquina virtual \_ E \_ no \_ Mostrar</dt> <dt>0xA0040850</dt> </dl>      | No se puede encontrar una pantalla válida para la máquina virtual.<br/>     |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>      | Se produjo un error inesperado.<br/>                             |



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

 

