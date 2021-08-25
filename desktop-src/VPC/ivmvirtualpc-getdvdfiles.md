---
title: Método IVMVirtualPC GetDVDFiles (VPCCOMInterfaces.h)
description: Recupera una matriz de archivos DVD conocidos.
ms.assetid: 9fe2191f-c5c0-464d-a190-29b2aba69682
keywords:
- Método GetDVDFiles de Pc virtual
- Método GetDVDFiles pc virtual , interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , Método GetDVDFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetDVDFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 585b1558c5a0692d4f9a3d5d8371cd0b7e5a692596c06605e7d86eadf377cf45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864125"
---
# <a name="ivmvirtualpcgetdvdfiles-method"></a>IVMVirtualPC::GetDVDFiles (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera una matriz de archivos DVD conocidos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDVDFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outDVDFileList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*inAdditionalSearchPaths* \[ En\]
</dt> <dd>

Estas rutas de acceso se buscarán junto con las rutas de acceso establecidas en la [**propiedad IVMVirtualPC::SearchPaths.**](ivmvirtualpc-searchpaths.md)

</dd> <dt>

*outDVDFileList* \[ out, retval\]
</dt> <dd>

Matriz de archivos de DVD virtual que se encuentran en las rutas de búsqueda especificadas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                        | Descripción                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                | El *parámetro outDVDFileList* es **NULL.**<br/>                                          |
| <dl> <dt>**E \_ Invalidarg**</dt> <dt>0x80000003</dt> </dl>                             | El *parámetro inAdditionalSearchPaths* no es una matriz de cadenas.<br/>                  |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |
| <dl> <dt>**Máquina virtual \_ E \_ HARDWARE \_ VIRTUALIZATION \_ DISABLED**</dt> <dt>0xA0040951</dt> </dl> | El procesador no admite extensiones de Virtualización acelerada por hardware (HAV).<br/> |



 

## <a name="remarks"></a>Comentarios

Las rutas de búsqueda usadas para recuperar la matriz de archivos incluirán las establecidas anteriormente por [**IVMVirtualPC::SearchPaths,**](ivmvirtualpc-searchpaths.md) además de las especificadas por el parámetro *inAdditionalSearchPaths* y la ubicación del instalador para el módulo de componentes de integración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC se define como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

