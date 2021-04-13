---
title: Método IVMVirtualPC CreateFloppyDiskImage (VPCCOMInterfaces. h)
description: Crea un archivo de imagen de disquete.
ms.assetid: 474e86a4-2019-41bd-9361-e494291d1961
keywords:
- Método CreateFloppyDiskImage Virtual PC
- Método CreateFloppyDiskImage Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método CreateFloppyDiskImage
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
ms.openlocfilehash: 5ff94ba5cb922aeb75f4effac413bb83b080b3fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492041"
---
# <a name="ivmvirtualpccreatefloppydiskimage-method"></a>IVMVirtualPC:: CreateFloppyDiskImage (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

*imagePath* \[ de\]
</dt> <dd>

Ruta de acceso completa al nuevo archivo de imagen de disco. Si no existe, se creará la carpeta contenedora.

</dd> <dt>

*imageType* \[ de\]
</dt> <dd>

El tipo de imagen de disquete que se va a crear. Solo se admiten **vmFloppyDiskImage \_ LowDensity** (1) y **vmFloppyDiskImage \_ HighDensity** (2). Vea [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                                                                                                         | La operación se realizó correctamente.<br/>                                                                                                                  |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                    | El parámetro *imagePath* es **null**.<br/>                                                                                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | El parámetro *imageType* no es [**vmFloppyDiskImage \_ LowDensity**](vmfloppydiskimagetype.md) (1) o **vmFloppyDiskImage \_ HighDensity** (2).<br/> |
| <dl> <dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt> </dl> | El sistema no puede encontrar la ruta de acceso especificada por el parámetro *imagePath* .<br/>                                                                        |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt> </dl>    | El parámetro *imagePath* contiene un carácter no válido (uno de " \* ?: <>/ \| " ").<br/>                                                           |
| <dl> <dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt> </dl>    | El parámetro *imagePath* especifica una ruta de acceso relativa o vacía. Se requiere una ruta de acceso absoluta.<br/>                                                   |
| <dl> <dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt> </dl> | La ruta de acceso especificada por el parámetro *imagePath* es demasiado larga. La longitud de la ruta de acceso debe ser inferior a 260 caracteres.<br/>                          |
| <dl> <dt>**HRESULT \_ DESDE \_ Win32 (error \_ ya \_ existe)**</dt> <dt>0x800700b7</dt> </dl>  | El archivo al que hace referencia el parámetro *imagePath* ya existe.<br/>                                                                               |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error de \_ disco \_ lleno)**</dt> <dt>0x80070070</dt> </dl>       | No hay suficiente espacio en el volumen del host para crear la imagen de disquete virtual.<br/>                                                        |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                            | Se ha producido un error inesperado.<br/>                                                                                                                  |
| <dl> <dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt> </dl>     | El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).<br/>                                                           |



 

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

 

