---
title: Método IVMVirtualPC GetFloppyDiskFiles (VPCCOMInterfaces. h)
description: Recupera una matriz de archivos de disquete virtual conocidos.
ms.assetid: c40f2780-eb84-4e0c-a493-1d1e5706cc8b
keywords:
- Método GetFloppyDiskFiles Virtual PC
- Método GetFloppyDiskFiles Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método GetFloppyDiskFiles
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
ms.openlocfilehash: 9759a3b909bb4f4ac179c166635185a701a8a16e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803733"
---
# <a name="ivmvirtualpcgetfloppydiskfiles-method"></a>IVMVirtualPC:: GetFloppyDiskFiles (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera una matriz de archivos de disquete virtual conocidos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFloppyDiskFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outFloppyDiskFileList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*inAdditionalSearchPaths* \[ de\]
</dt> <dd>

Estas rutas de acceso se buscarán junto con las rutas de acceso establecidas en la propiedad [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) .

</dd> <dt>

*outFloppyDiskFileList* \[ out, retval\]
</dt> <dd>

Matriz de archivos de disquete virtual encontrados en las rutas de acceso de búsqueda especificadas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                        | Descripción                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                | El parámetro *outFloppyDiskFileList* es **null**.<br/>                                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | El parámetro *inAdditionalSearchPaths* no es una matriz de cadenas.<br/>                  |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |
| <dl> <dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt> </dl> | El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).<br/> |



 

## <a name="remarks"></a>Observaciones

Las rutas de acceso de búsqueda que se usan para recuperar la matriz de archivos incluirán los establecidos anteriormente por [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) además de los especificados por el parámetro *inAdditionalSearchPaths* y la ubicación del instalador para el módulo Integration Components.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

