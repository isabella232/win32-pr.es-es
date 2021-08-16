---
title: Método IVMVirtualPC GetVirtualMachineFiles (VPCCOMInterfaces.h)
description: Recupera una matriz de archivos de configuración de máquina virtual conocidos.
ms.assetid: 38771573-66fa-408a-95db-1281efdf8b73
keywords:
- Método GetVirtualMachineFiles de Virtual PC
- Método GetVirtualMachineFiles Virtual PC , interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , Método GetVirtualMachineFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetVirtualMachineFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ae2f96fb0c289f155158c77cdf3e4a8df1cb83aa8a51e0329d9fcd835ea4d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998605"
---
# <a name="ivmvirtualpcgetvirtualmachinefiles-method"></a>IVMVirtualPC::GetVirtualMachineFiles (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera una matriz de archivos de configuración de máquina virtual conocidos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetVirtualMachineFiles(
  [in]          VARIANT      inAdditionalSearchPaths,
  [in]          VARIANT_BOOL inExcludedRegisteredVMs,
  [out, retval] VARIANT      *outVirtualMachineFileList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*inAdditionalSearchPaths* \[ En\]
</dt> <dd>

Estas rutas de acceso se buscarán junto con las rutas de acceso establecidas en las propiedades [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) e [**IVMVirtualPC::D efaultVMConfigurationPath.**](ivmvirtualpc-defaultvmconfigurationpath.md)

</dd> <dt>

*inExcludedRegisteredVMs* \[ En\]
</dt> <dd>

**TRUE** si las máquinas virtuales registradas deben excluirse de la devolución de la matriz *en el parámetro outVirtualMachineFileList* y **FALSE** en caso contrario.

</dd> <dt>

*outVirtualMachineFileList* \[ out, retval\]
</dt> <dd>

Matriz de cadenas de ruta de acceso para los archivos de configuración de máquina virtual que se encuentran en las rutas de acceso de búsqueda especificadas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                        | Descripción                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                | El *parámetro outVirtualMachineFileList* es **NULL.**<br/>                               |
| <dl> <dt>**E \_ InvalidarG**</dt> <dt>0x80000003</dt> </dl>                             | El *parámetro inAdditionalSearchPaths* no es una matriz de cadenas.<br/>                  |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |
| <dl> <dt>**Máquina virtual \_ E \_ HARDWARE \_ VIRTUALIZATION \_ DISABLED**</dt> <dt>0xA0040951</dt> </dl> | El procesador no admite extensiones de Virtualización acelerada por hardware (HAV).<br/> |



 

## <a name="remarks"></a>Comentarios

Las rutas de búsqueda usadas para recuperar la matriz de archivos de configuración incluirán las establecidas anteriormente por [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) e [**IVMVirtualPC::D efaultVMConfigurationPath,**](ivmvirtualpc-defaultvmconfigurationpath.md) además de las especificadas por el parámetro *inAdditionalSearchPaths.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC se define como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

