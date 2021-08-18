---
title: Propiedad IVMVirtualPC Version (VPCCOMInterfaces.h)
description: Recupera la versión de esta instancia de Windows Virtual PC.
ms.assetid: efcd5e71-8752-45a2-8138-4bc214762f39
keywords:
- Propiedad de versión Virtual PC
- Propiedad de versión Virtual PC , interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , propiedad Version
topic_type:
- apiref
api_name:
- IVMVirtualPC.Version
- IVMVirtualPC.get_Version
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fad1f72c5a87e047001f013c70e5b730bcd06b342d8e56cc390b62b2f284ae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591698"
---
# <a name="ivmvirtualpcversion-property"></a>Propiedad IVMVirtualPC::Version

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la versión de esta instancia de Windows Virtual PC.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Version(
  [out, retval] BSTR *version
);
```



## <a name="property-value"></a>Valor de propiedad

La versión.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                           | Significado                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                                | El parámetro es **NULL.**<br/>                                                           |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |
| <dl> <dt>Máquina virtual \_ E \_ HARDWARE VIRTUALIZATION DISABLED \_ \_ 0xA0040951</dt> <dt></dt> </dl> | El procesador no admite extensiones de Virtualización acelerada por hardware (HAV).<br/> |



## <a name="remarks"></a>Comentarios

La Windows de la versión de Virtual PC se devuelve como un valor de cadena con el formato siguiente: "*v*. *s*. *bbb*. *tee*", donde *v* es el número de versión principal, *s* es el número de versión secundaria, *bbb* es el número de compilación, *t* es el tipo de compilación (0 = compilación de versión) y *ee* es la edición del servidor (SE = Standard Edition, EE = Enterprise Edition).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC se define como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

