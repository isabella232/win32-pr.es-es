---
title: Método IVMVirtualPC GetFstonepyDiskFiles (VPCCOMInterfaces.h)
description: Recupera una matriz de archivos de disquete virtuales conocidos.
ms.assetid: c40f2780-eb84-4e0c-a493-1d1e5706cc8b
keywords:
- Método Virtual PC getFstonepyDiskFiles
- Método GetFstonepyDiskFiles para PC virtual, interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , Método GetFstonepyDiskFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetFloppyDiskFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d1c5b2e42fd079b345278050ed7c0cdba52de79eb1dace6078ebc97549dbe9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118842791"
---
# <a name="ivmvirtualpcgetfloppydiskfiles-method"></a>IVMVirtualPC::GetFstonepyDiskFiles (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera una matriz de archivos de disquete virtuales conocidos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFloppyDiskFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outFloppyDiskFileList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*inAdditionalSearchPaths* \[ En\]
</dt> <dd>

Estas rutas de acceso se buscarán junto con las rutas de acceso establecidas en la [**propiedad IVMVirtualPC::SearchPaths.**](ivmvirtualpc-searchpaths.md)

</dd> <dt>

*outFstonepyDiskFileList* \[ out, retval\]
</dt> <dd>

Matriz de archivos de disquete virtual que se encuentran en las rutas de búsqueda especificadas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                        | Descripción                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                | El *parámetro outFstonepyDiskFileList* es **NULL.**<br/>                                   |
| <dl> <dt>**E \_ Invalidarg**</dt> <dt>0x80000003</dt> </dl>                             | El *parámetro inAdditionalSearchPaths* no es una matriz de cadenas.<br/>                  |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |
| <dl> <dt>**Máquina virtual \_ E \_ \_ VIRTUALIZACIÓN DE HARDWARE \_ DESHABILITADA**</dt> <dt>0xA0040951</dt> </dl> | El procesador no admite extensiones de virtualización acelerada de hardware (HAV).<br/> |



 

## <a name="remarks"></a>Comentarios

Las rutas de búsqueda usadas para recuperar la matriz de archivos incluirán las establecidas previamente por [**IVMVirtualPC::SearchPaths,**](ivmvirtualpc-searchpaths.md) además de las especificadas por el parámetro *inAdditionalSearchPaths* y la ubicación del instalador del módulo de componentes de integración.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

