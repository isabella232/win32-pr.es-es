---
title: Método IVMHardDisk Convert (VPCCOMInterfaces.h)
description: Convierte un disco duro virtual de tamaño fijo en un disco duro virtual de expansión dinámica o convierte un disco duro virtual de expansión dinámica en un disco duro virtual de tamaño fijo.
ms.assetid: 0dee802a-1cac-499e-918a-7dbb6c98415f
keywords:
- Conversión del método Virtual PC
- Conversión del método Virtual PC, interfaz IVMHardDisk
- IVMHardDisk interface Virtual PC , Método Convert
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
ms.openlocfilehash: e509c683ef86e169eb07d661c9682d8ed67204bcc7e1651d2d6370ee4be82f09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593888"
---
# <a name="ivmharddiskconvert-method"></a>IVMHardDisk::Convert (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

*convertedDiskImagePath* \[ En\]
</dt> <dd>

Ruta de acceso al archivo de imagen de disco de destino.

</dd> <dt>

*convertedDiskImageType* \[ En\]
</dt> <dd>

Tipo de la imagen de disco de destino. Para obtener una lista de valores, [**consulte VMHardDiskType.**](vmharddisktype.md)

</dd> <dt>

*convertTask* \[ out, retval\]
</dt> <dd>

Objeto [**IVMTask que**](ivmtask.md) se usa para realizar un seguimiento de la finalización del proceso de conversión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                              | Descripción                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                                    | La operación se realizó correctamente.<br/>                                                                                                        |
| <dl> <dt>**E \_ InvalidarG**</dt> <dt>0x80000003</dt> </dl>                                   | El *parámetro convertedDiskImagePath* está vacío o falta la extensión .vhd en el nombre de archivo.<br/>                                      |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                      | Un parámetro es **NULL.**<br/>                                                                                                             |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(RUTA DE ACCESO DE ERROR \_ \_ NO \_ ENCONTRADA)**</dt> <dt>0X80070003</dt> </dl>   | El sistema no puede encontrar la ruta de acceso especificada por el *parámetro convertedDiskImagePath.*<br/>                                                 |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ NOMBRE NO \_ VÁLIDO)**</dt> <dt>0x8007007b</dt> </dl>      | El *parámetro convertedDiskImagePath* contiene un carácter no válido (uno de " \* ?<>/ \| ":").<br/>                                    |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>      | El *parámetro convertedDiskImagePath* especifica una ruta de acceso vacía o relativa. Se requiere una ruta de acceso absoluta.<br/>                            |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl>   | La ruta de acceso especificada por *el parámetro convertedDiskImagePath* es demasiado larga. La ruta de acceso debe tener menos **de MAX \_ PATH** (260) caracteres.<br/> |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(INFRACCIÓN \_ DE USO COMPARTIDO DE \_ ERRORES)**</dt> <dt>0x80070020</dt> </dl> | El disco duro virtual al que hace referencia este objeto está en uso o el elemento primario de este disco duro virtual está en uso.<br/>                  |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ DISK \_ FULL)**</dt> <dt>0x80070070</dt> </dl>         | El volumen host no tiene suficiente espacio para convertir este disco duro virtual.<br/>                                                        |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ YA \_ EXISTE)**</dt> <dt>0X800700B7</dt> </dl>    | El archivo al que hace referencia *el parámetro convertedDiskImagePath* ya existe.<br/>                                                        |
| <dl> <dt>**Máquina virtual \_ E \_ ERROR DE TIPO DE \_ \_ \_ IMAGEN**</dt> <dt>DE HD 0xA004067B</dt> </dl>                   | El *parámetro convertedDiskImagePath* debe ser **vmDiskType \_ Dynamic** o **vmDiskType \_ FixedSize.**<br/>                          |
| <dl> <dt>**Máquina virtual \_ E \_ ARCHIVOS HD NO \_ \_ VÁLIDOs**</dt> <dt>0xA0040682</dt> </dl>                        | La imagen de disco duro virtual a la que hace referencia este [**objeto IVMHardDisk**](ivmharddisk.md) no parece ser una imagen válida.<br/>          |
| <dl> <dt>**Máquina virtual \_ NO \_ SE ENCONTRÓ LA RUTA DE \_ \_ \_ ACCESO**</dt> <dt>PRIMARIA 0XA0040677</dt> </dl>                 | El elemento primario del disco duro virtual al que hace referencia este objeto no existe.<br/>                                                        |
| <dl> <dt>**Máquina virtual \_ E \_ APP \_ SHUTTING \_ DOWN**</dt> <dt>0xA0040209</dt> </dl>                      | La imagen de disco duro virtual no se puede convertir porque la aplicación se está cerrando.<br/>                                            |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                              | Se produjo un error inesperado.<br/>                                                                                                    |



 

## <a name="remarks"></a>Observaciones

El archivo de origen se deja intacto después del proceso de conversión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHardDisk se define como \_ ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

