---
title: Método IVMVirtualPC CreateFstonepyDiskImage (VPCCOMInterfaces.h)
description: Crea un archivo de imagen de disquete.
ms.assetid: 474e86a4-2019-41bd-9361-e494291d1961
keywords:
- CreateFstonepyDiskImage, método Virtual PC
- Método CreateFstonepyDiskImage virtual PC , interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , Método CreateFstonepyDiskImage
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFloppyDiskImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1715bd9adc5fdcfae355b5992cb800a6d38a0889ed92745314daa6b2cfc2d8b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124665"
---
# <a name="ivmvirtualpccreatefloppydiskimage-method"></a>IVMVirtualPC::CreateFstonepyDiskImage (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Crea un archivo de imagen de disquete.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateFloppyDiskImage(
  [in] BSTR                  imagePath,
  [in] VMFloppyDiskImageType imageType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*imagePath* \[ En\]
</dt> <dd>

Ruta de acceso completa al nuevo archivo de imagen de disco. La carpeta que lo contiene se creará si no existe.

</dd> <dt>

*imageType* \[ En\]
</dt> <dd>

Tipo de imagen de disquete que se creará. Solo **se admiten vmFstonepyDiskImage \_ LowDensity** (1) y **vmFstonepyDiskImage \_ HighDensity** (2). Vea [**VMFstonepyDiskImageType.**](vmfloppydiskimagetype.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                                                                         | La operación se realizó correctamente.<br/>                                                                                                                  |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                    | El *parámetro imagePath* es **NULL.**<br/>                                                                                                         |
| <dl> <dt>**E \_ Invalidarg**</dt> <dt>0x80000003</dt> </dl>                                 | El *parámetro imageType* no es [**vmFstonepyDiskImage \_ LowDensity**](vmfloppydiskimagetype.md) (1) ni **vmFstonepyDiskImage \_ HighDensity** (2).<br/> |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32 (RUTA DE ACCESO DE ERROR \_ \_ NO \_ ENCONTRADA)**</dt> <dt>0X80070003</dt> </dl> | El sistema no puede encontrar la ruta de acceso especificada por el *parámetro imagePath.*<br/>                                                                        |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ INVALID \_ NAME) 0X8007007B**</dt> <dt></dt> </dl>    | El *parámetro imagePath* contiene un carácter no válido (uno de " \* ?:<>/ \| "").<br/>                                                           |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0X800700A1</dt> </dl>    | El *parámetro imagePath* especifica una ruta de acceso vacía o relativa. Se requiere una ruta de acceso absoluta.<br/>                                                   |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | La ruta de acceso especificada por el *parámetro imagePath* es demasiado larga. La longitud de la ruta de acceso debe tener menos de 260 caracteres.<br/>                          |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32 (ERROR \_ \_ YA EXISTE) 0X800700B7**</dt> <dt></dt> </dl>  | El archivo al que hace referencia el parámetro *imagePath* ya existe.<br/>                                                                               |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ DISK \_ FULL) 0X80070070**</dt> <dt></dt> </dl>       | No hay suficiente espacio en el volumen del host para crear la imagen de disquete virtual.<br/>                                                        |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Se ha producido un error inesperado.<br/>                                                                                                                  |
| <dl> <dt>**Máquina virtual \_ E \_ HARDWARE \_ VIRTUALIZATION \_ DISABLED**</dt> <dt>0xA0040951</dt> </dl>     | El procesador no admite extensiones de Virtualización acelerada por hardware (HAV).<br/>                                                           |



 

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

 

