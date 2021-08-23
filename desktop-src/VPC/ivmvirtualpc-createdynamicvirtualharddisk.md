---
title: Método IVMVirtualPC CreateDynamicVirtualHardDisk (VPCCOMInterfaces.h)
description: Crea un disco duro virtual que cambia de tamaño dinámicamente.
ms.assetid: 2373ac41-c4c4-44c6-93e1-92814cd40b81
keywords:
- Método Virtual PC CreateDynamicVirtualHardDisk
- Método Virtual PC CreateDynamicVirtualHardDisk, interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , Método CreateDynamicVirtualHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateDynamicVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6de505f2e8b47bc36b7537a3abcdab1f07e7551a8c5ed9caee9aed100288df51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998655"
---
# <a name="ivmvirtualpccreatedynamicvirtualharddisk-method"></a>IVMVirtualPC::CreateDynamicVirtualHardDisk (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Crea un disco duro virtual que cambia de tamaño dinámicamente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateDynamicVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          long    size,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*imagePath* \[ En\]
</dt> <dd>

Ruta de acceso completa al nuevo archivo de imagen de disco. La carpeta que contiene se creará si no existe.

</dd> <dt>

*size* \[ En\]
</dt> <dd>

Tamaño de la imagen, en megabytes. Este valor puede ser como máximo de 2.088.960 MB (2040 GB).

</dd> <dt>

*diskTask* \[ out, retval\]
</dt> <dd>

Objeto [**IVMTask**](ivmtask.md) que se usa para realizar un seguimiento de la creación de la imagen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                                                                                                                                                                       |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                    | Un parámetro es **NULL.**<br/>                                                                                                                                                                                                            |
| <dl> <dt>**E \_ InvalidarG**</dt> <dt>0x80000003</dt> </dl>                                 | El *parámetro size* es menor o igual que 0.<br/>                                                                                                                                                                                    |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(RUTA DE ACCESO DE ERROR \_ \_ NO \_ ENCONTRADA)**</dt> <dt>0X80070003</dt> </dl> | El sistema no puede encontrar la ruta de acceso especificada por el *parámetro imagePath.*<br/>                                                                                                                                                             |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ UNIDAD NO \_ VÁLIDA)**</dt> <dt>0x8007000f</dt> </dl>   | El archivo especificado por el *parámetro imagePath* está en un CD-ROM o DVD-ROM.<br/>                                                                                                                                                          |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ NOMBRE NO \_ VÁLIDO)**</dt> <dt>0x8007007b</dt> </dl>    | El *parámetro imagePath* contiene un carácter no válido (uno de " \* ?:<>/ \| "").<br/>                                                                                                                                                |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | El parámetro *imagePath* especifica una ruta de acceso vacía o relativa. Al menos uno de los parámetros debe ser una ruta de acceso absoluta.<br/>                                                                                                        |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | La ruta de acceso especificada por el *parámetro imagePath* es demasiado larga. La longitud de la ruta de acceso debe ser inferior a 260 caracteres.<br/>                                                                                                               |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ YA \_ EXISTE)**</dt> <dt>0X800700B7</dt> </dl>  | El archivo al que hace referencia el *parámetro imagePath* ya existe.<br/>                                                                                                                                                                    |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ DISK \_ FULL)**</dt> <dt>0x80070070</dt> </dl>       | La imagen de disco duro virtual que se expande dinámicamente necesita al menos 8 MB de espacio libre en el volumen del host.<br/>                                                                                                                                      |
| <dl> <dt>**Máquina virtual \_ E \_ TAMAÑO DE IMAGEN \_ \_ \_ DEMASIADO**</dt> GRANDE <dt>0xA0040683</dt> </dl>                | El tamaño *del parámetro* debe ser inferior a 2 088 960 MB. Si el formato es FAT16, el tamaño debe ser inferior a 2000 MB.<br/>                                                                                                                   |
| <dl> <dt>**Máquina virtual \_ E \_ TAMAÑO DE IMAGEN DEMASIADO \_ \_ \_ PEQUEÑO**</dt> <dt>0xA0040684</dt> </dl>                | Las imágenes de disco duro virtual con formato FAT16 y sin formato deben tener al menos 3 MB. Las imágenes de disco duro virtual con formato FAT32 deben tener al menos 514 MB.<br/>                                                                                   |
| <dl> <dt>**Máquina virtual \_ E \_ FILE TOO LARGE FOR \_ \_ \_ \_ VOLUME**</dt> <dt>0XA0040679</dt> </dl>          | El volumen host no puede admitir un archivo de este tamaño si la imagen de disco duro virtual que se expande dinámicamente se expande hasta su límite total. El tamaño máximo de archivo para un volumen FAT32 es de 4 GB. El tamaño máximo de archivo para un volumen FAT16 es de 2 GB.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ APP \_ SHUTTING \_ DOWN**</dt> <dt>0xA0040209</dt> </dl>                    | No se puede crear el disco duro virtual después de que la aplicación haya empezado a cerrarse.<br/>                                                                                                                                            |
| <dl> <dt>**Máquina virtual \_ E \_ \_ VIRTUALIZACIÓN DE HARDWARE \_ DESHABILITADA**</dt> <dt>0xA0040951</dt> </dl>     | El procesador no admite extensiones de virtualización acelerada de hardware (HAV).<br/>                                                                                                                                                |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                                                                                                                                   |



 

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

 

