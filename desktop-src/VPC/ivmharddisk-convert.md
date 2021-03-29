---
title: Método Convert de IVMHardDisk (VPCCOMInterfaces. h)
description: Convierte un disco duro virtual de tamaño fijo en un disco duro virtual de expansión dinámica o convierte un disco duro virtual de expansión dinámica en un disco duro virtual de tamaño fijo.
ms.assetid: 0dee802a-1cac-499e-918a-7dbb6c98415f
keywords:
- Convertir el método en Virtual PC
- Método Convert Virtual PC, interfaz IVMHardDisk
- Interfaz IVMHardDisk Virtual PC, método Convert
topic_type:
- apiref
api_name:
- IVMHardDisk.Convert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398cf4a2f3b366709c009885bf2c2767828fee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492695"
---
# <a name="ivmharddiskconvert-method"></a>IVMHardDisk:: Convert (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Convierte un disco duro virtual de tamaño fijo en un disco duro virtual de expansión dinámica o convierte un disco duro virtual de expansión dinámica en un disco duro virtual de tamaño fijo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Convert(
  [in]          BSTR           convertedDiskImagePath,
  [in]          VMHardDiskType convertedDiskImageType,
  [out, retval] IVMTask        **convertTask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*convertedDiskImagePath* \[ de\]
</dt> <dd>

Ruta de acceso al archivo de imagen de disco de destino.

</dd> <dt>

*convertedDiskImageType* \[ de\]
</dt> <dd>

El tipo de la imagen de disco de destino. Para obtener una lista de valores, vea [**VMHardDiskType**](vmharddisktype.md).

</dd> <dt>

*convertTask* \[ out, retval\]
</dt> <dd>

Objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento de la finalización del proceso de conversión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                              | Descripción                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                                    | La operación se realizó correctamente.<br/>                                                                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                   | El parámetro *convertedDiskImagePath* está vacío o falta la extensión. vhd en el nombre de archivo.<br/>                                      |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                      | Un parámetro es **null**.<br/>                                                                                                             |
| <dl> <dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt> </dl>   | El sistema no puede encontrar la ruta de acceso especificada por el parámetro *convertedDiskImagePath* .<br/>                                                 |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt> </dl>      | El parámetro *convertedDiskImagePath* contiene un carácter no válido (uno de " \* ? <>/ \| ": ").<br/>                                    |
| <dl> <dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt> </dl>      | El parámetro *convertedDiskImagePath* especifica una ruta de acceso relativa o vacía. Se requiere una ruta de acceso absoluta.<br/>                            |
| <dl> <dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt> </dl>   | La ruta de acceso especificada por el parámetro *convertedDiskImagePath* es demasiado larga. La ruta de acceso debe ser menor que el número máximo de caracteres de **\_ ruta de acceso** (260).<br/> |
| <dl> <dt>**HRESULT \_ De \_ Win32 ( \_ \_ infracción de uso compartido de errores)**</dt> <dt>0x80070020</dt> </dl> | El disco duro virtual al que hace referencia este objeto está en uso o el primario de este disco duro virtual está en uso.<br/>                  |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error de \_ disco \_ lleno)**</dt> <dt>0x80070070</dt> </dl>         | El volumen del host no tiene suficiente espacio para convertir este disco duro virtual.<br/>                                                        |
| <dl> <dt>**HRESULT \_ DESDE \_ Win32 (error \_ ya \_ existe)**</dt> <dt>0x800700b7</dt> </dl>    | El archivo al que hace referencia el parámetro *convertedDiskImagePath* ya existe.<br/>                                                        |
| <dl> <dt>**Máquina virtual \_ E es el \_ \_ \_ \_ tipo de imagen HD**</dt> <dt>0xA004067B</dt> </dl>                   | El parámetro *convertedDiskImagePath* debe ser **VmDiskType \_ Dynamic** o **vmDiskType \_ FixedSize**.<br/>                          |
| <dl> <dt>**Máquina virtual \_ E 0xA0040682 de \_ \_ \_ archivo HD no válido**</dt> <dt></dt> </dl>                        | Parece que la imagen de disco duro virtual a la que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) no es una imagen válida.<br/>          |
| <dl> <dt>**Máquina virtual \_ \_ \_ \_ No \_ se encontró la ruta de acceso principal E**</dt> <dt>0xA0040677</dt> </dl>                 | No existe el elemento primario del disco duro virtual al que hace referencia este objeto.<br/>                                                        |
| <dl> <dt>**Máquina virtual \_ E \_ \_ \_**</dt> <dt>0xA0040209</dt> de la aplicación </dl>                      | No se puede convertir la imagen de disco duro virtual porque la aplicación se está cerrando.<br/>                                            |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                              | Se produjo un error inesperado.<br/>                                                                                                    |



 

## <a name="remarks"></a>Observaciones

El archivo de código fuente se deja intacto después del proceso de conversión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk se define como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

