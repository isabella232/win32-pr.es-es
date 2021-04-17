---
title: Método IVMVirtualPC CreateDifferencingVirtualHardDisk (VPCCOMInterfaces. h)
description: Crea un disco duro virtual de diferenciación.
ms.assetid: 6a33aa6f-a0e8-45d8-bdc1-0864561db162
keywords:
- Método CreateDifferencingVirtualHardDisk Virtual PC
- Método CreateDifferencingVirtualHardDisk Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método CreateDifferencingVirtualHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateDifferencingVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2bab178d64008b236988bfb723bd75a09a7edaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696003"
---
# <a name="ivmvirtualpccreatedifferencingvirtualharddisk-method"></a>IVMVirtualPC:: CreateDifferencingVirtualHardDisk (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Crea un disco duro virtual de diferenciación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateDifferencingVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          BSTR    parentPath,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*imagePath* \[ de\]
</dt> <dd>

Ruta de acceso al nuevo archivo de imagen de disco. Si no existe, se creará la carpeta contenedora.

</dd> <dt>

*parentPath* \[ de\]
</dt> <dd>

Ruta de acceso al archivo de imagen de disco principal.

</dd> <dt>

*diskTask* \[ out, retval\]
</dt> <dd>

Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento de la creación de la imagen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                                                                                                                                                                       |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                    | Un parámetro es **null**.<br/>                                                                                                                                                                                                            |
| <dl> <dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt> </dl> | El sistema no puede encontrar la ruta de acceso especificada por el parámetro *imagePath* o *parentPath* .<br/>                                                                                                                                             |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ unidad no válida)**</dt> <dt>0x8007000f</dt> </dl>   | El archivo especificado por el parámetro *imagePath* se encuentra en un CD-ROM o DVD-ROM.<br/>                                                                                                                                                          |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt> </dl>    | El parámetro *imagePath* o *parentPath* contiene un carácter no válido (uno de " \* ?: <>/ \| " ").<br/>                                                                                                                                |
| <dl> <dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt> </dl>    | El parámetro *imagePath* y *parentPath* especifica una ruta de acceso relativa o vacía. Al menos uno de los parámetros debe ser una ruta de acceso absoluta.<br/>                                                                                       |
| <dl> <dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt> </dl> | La ruta de acceso especificada por los parámetros *imagePath* o *parentPath* es demasiado larga. La longitud de la ruta de acceso debe ser inferior a 260 caracteres.<br/>                                                                                              |
| <dl> <dt>**HRESULT \_ DESDE \_ Win32 (error \_ ya \_ existe)**</dt> <dt>0x800700b7</dt> </dl>  | El archivo al que hace referencia el parámetro *imagePath* ya existe.<br/>                                                                                                                                                                    |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error de \_ disco \_ lleno)**</dt> <dt>0x80070070</dt> </dl>       | La imagen de disco duro virtual de expansión dinámica necesita al menos 8 MB de espacio libre en el volumen del host.<br/>                                                                                                                                      |
| <dl> <dt>**Máquina virtual \_ E \_ tamaño de imagen \_ \_ demasiado \_ grande**</dt> <dt>0xA0040683</dt> </dl>                | El *tamaño* del parámetro debe ser inferior a 2.088.960 MB. Si el formato es FAT16, el tamaño debe ser inferior a 2000 MB.<br/>                                                                                                                   |
| <dl> <dt>**Máquina virtual \_ E \_ tamaño de imagen \_ \_ demasiado \_ pequeño**</dt> <dt>0xA0040684</dt> </dl>                | Las imágenes de disco duro virtual con formato FAT16 y sin formato deben ser de al menos 3 MB. Las imágenes de disco duro virtual con formato FAT32 deben ser de al menos 514 MB.<br/>                                                                                   |
| <dl> <dt>**Máquina virtual \_ El \_ archivo E \_ es demasiado \_ grande \_ para el \_ volumen**</dt> <dt>0xA0040679</dt> </dl>          | El volumen del host no puede admitir un archivo este tamaño si la imagen de disco duro virtual de expansión dinámica se expande hasta su límite completo. El tamaño de archivo máximo para un volumen FAT32 es 4 GB. El tamaño de archivo máximo para un volumen FAT16 es 2 GB.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ \_ \_**</dt> <dt>0xA0040209</dt> de la aplicación </dl>                    | No se puede crear el disco duro virtual después de que la aplicación haya empezado a cerrarse.<br/>                                                                                                                                            |
| <dl> <dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt> </dl>     | El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).<br/>                                                                                                                                                |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Observaciones

Aunque *imagePath* o *parentPath* puede ser una ruta de acceso relativa, al menos uno de estos valores debe ser una ruta de acceso absoluta. Si un parámetro de ruta de acceso es una ruta de acceso relativa, se supone que es relativo al otro parámetro de ruta de acceso.

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

 

