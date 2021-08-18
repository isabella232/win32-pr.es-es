---
title: Método IVMVirtualPC GetHardDiskFiles (VPCCOMInterfaces.h)
description: Recupera una matriz de archivos de disco duro virtual conocidos.
ms.assetid: 3f949ebc-5974-4919-84a2-8411f558f85f
keywords:
- Equipo virtual del método GetHardDiskFiles
- Método GetHardDiskFiles para PC virtual, interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , Método GetHardDiskFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDiskFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 902cd124db27ae65b8f589ded8b2b3188a7e0df67b0ff20071abd04daf5ab894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136578"
---
# <a name="ivmvirtualpcgetharddiskfiles-method"></a>IVMVirtualPC::GetHardDiskFiles (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera una matriz de archivos de disco duro virtual conocidos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetHardDiskFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outHardDiskFileList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*inAdditionalSearchPaths* \[ En\]
</dt> <dd>

Estas rutas de acceso se buscarán junto con las rutas de acceso establecidas en la [**propiedad IVMVirtualPC::SearchPaths.**](ivmvirtualpc-searchpaths.md)

</dd> <dt>

*outHardDiskFileList* \[ out, retval\]
</dt> <dd>

Matriz de cadenas de ruta de acceso para los archivos de disco duro virtual que se encuentran en las rutas de acceso de búsqueda especificadas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                        | Descripción                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                | El *parámetro outHardDiskFileList* es **NULL.**<br/>                                     |
| <dl> <dt>**E \_ InvalidarG**</dt> <dt>0x80000003</dt> </dl>                             | El *parámetro inAdditionalSearchPaths* no es una matriz de cadenas.<br/>                  |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |
| <dl> <dt>**Máquina virtual \_ E \_ \_ VIRTUALIZACIÓN DE HARDWARE \_ DESHABILITADA**</dt> <dt>0xA0040951</dt> </dl> | El procesador no admite extensiones de virtualización acelerada de hardware (HAV).<br/> |



 

## <a name="remarks"></a>Comentarios

Las rutas de búsqueda usadas para recuperar la matriz de archivos incluirán las establecidas anteriormente por [**IVMVirtualPC::SearchPaths,**](ivmvirtualpc-searchpaths.md) además de las especificadas por el parámetro *inAdditionalSearchPaths.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC se define como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

