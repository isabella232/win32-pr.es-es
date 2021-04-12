---
title: Método Mergeto de IVMHardDisk (VPCCOMInterfaces. h)
description: Combina un disco duro virtual de diferenciación con todos sus elementos primarios.
ms.assetid: 3c63f892-7c05-4ed6-a59a-914a921ec391
keywords:
- Método mergeto Virtual PC
- Método mergeto Virtual PC, interfaz IVMHardDisk
- Interfaz IVMHardDisk Virtual PC, método Mergeto
topic_type:
- apiref
api_name:
- IVMHardDisk.MergeTo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d0db44388c8ee021fa8cc8c8fdbfe2c434833f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150381"
---
# <a name="ivmharddiskmergeto-method"></a>IVMHardDisk:: Mergeto (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Combina un disco duro virtual de diferenciación con todos sus elementos primarios (hasta el disco duro virtual primario raíz incluido) en un nuevo archivo de disco duro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MergeTo(
  [in]          BSTR           newDiskImagePath,
  [in]          VMHardDiskType newDiskImageType,
  [out, retval] IVMTask        **mergeTask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newDiskImagePath* \[ de\]
</dt> <dd>

La ruta de acceso a la nueva imagen de disco de destino en la que se combinarán las imágenes de disco seleccionadas.

</dd> <dt>

*newDiskImageType* \[ de\]
</dt> <dd>

El tipo de nueva imagen de disco de destino. Los tipos de imagen permitidos para la nueva imagen de disco de destino son **vmDiskType \_ Dynamic** y **vmDiskType \_ FixedSize**. Para obtener más información, vea [**VMHardDiskType**](vmharddisktype.md).

</dd> <dt>

*mergeTask* \[ out, retval\]
</dt> <dd>

Objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento de la finalización del proceso de combinación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                                    | La operación se realizó correctamente.<br/>                                                                                                                                                                                                                                                                      |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                      | Un parámetro es **null**.<br/>                                                                                                                                                                                                                                                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                   | El parámetro *newDiskImagePath* está vacío.<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)**</dt> <dt>0x80070002</dt> </dl>   | El sistema no encuentra el archivo especificado por el parámetro *newDiskImagePath* .<br/>                                                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt> </dl>   | El sistema no puede encontrar la ruta de acceso especificada por el parámetro *newDiskImagePath* .<br/>                                                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt> </dl>      | El parámetro *newDiskImagePath* contiene un carácter no válido (uno de los siguientes: " \* ? <>/ \| ": ").<br/>                                                                                                                                                                                         |
| <dl> <dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt> </dl>      | El parámetro *newDiskImagePath* especifica una ruta de acceso relativa o vacía. Se requiere una ruta de acceso absoluta.<br/>                                                                                                                                                                                                |
| <dl> <dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt> </dl>   | La ruta de acceso especificada por el parámetro *newDiskImagePath* es demasiado larga. La ruta de acceso debe tener menos de 260 caracteres.<br/>                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ De \_ Win32 ( \_ \_ infracción de uso compartido de errores)**</dt> <dt>0x80070020</dt> </dl> | El disco duro virtual al que hace referencia este objeto está en uso o el primario de este disco duro virtual está en uso.<br/>                                                                                                                                                                                |
| <dl> <dt>**Máquina virtual \_ E es el \_ \_ \_ \_ tipo de imagen HD**</dt> <dt>0xA004067B</dt> </dl>                   | Este error se debe a que la imagen de disco duro virtual a la que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) no es una imagen de disco de diferenciación, o bien porque el parámetro *newDiskImageType* no es uno de los valores aceptados, **vmDiskType \_ Dynamic** o **vmDiskType \_ FixedSize**.<br/> |
| <dl> <dt>**HRESULT \_ DESDE \_ Win32 (error \_ ya \_ existe)**</dt> <dt>0x800700b7</dt> </dl>    | El archivo al que hace referencia el parámetro *newDiskImagePath* ya existe.<br/>                                                                                                                                                                                                                            |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error de \_ disco \_ lleno)**</dt> <dt>0x80070070</dt> </dl>         | El volumen del host no tiene suficiente espacio para fusionar mediante combinación este disco duro virtual.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**Máquina virtual \_ \_ \_ \_ No \_ se encontró la ruta de acceso principal E**</dt> <dt>0xA0040677</dt> </dl>                 | No existe el elemento primario del disco duro virtual al que hace referencia este objeto.<br/>                                                                                                                                                                                                                      |
| <dl> <dt>**Máquina virtual \_ E \_ \_ \_**</dt> <dt>0xA0040209</dt> de la aplicación </dl>                      | No se puede fusionar mediante combinación la imagen de disco duro virtual porque se está cerrando.<br/>                                                                                                                                                                                                             |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                              | Se produjo un error inesperado.<br/>                                                                                                                                                                                                                                                                  |



 

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

 

