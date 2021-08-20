---
title: Método IVMHardDisk MergeTo (VPCCOMInterfaces.h)
description: Combina un disco duro virtual de diferenciación con todos sus padres.
ms.assetid: 3c63f892-7c05-4ed6-a59a-914a921ec391
keywords:
- MergeTo, método Virtual PC
- Método MergeTo De PC virtual, interfaz IVMHardDisk
- IVMHardDisk interface Virtual PC , MergeTo method
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
ms.openlocfilehash: 19f54c3e7cfcd328adcea355e90ff60d92590fb694915a3e682a6240b656e655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123758"
---
# <a name="ivmharddiskmergeto-method"></a>IVMHardDisk::MergeTo (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Combina un disco duro virtual de diferenciación con todos sus elementos primarios (hasta e incluyendo el disco duro virtual principal raíz) en un nuevo archivo de disco duro.

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

*newDiskImagePath* \[ En\]
</dt> <dd>

Ruta de acceso a la nueva imagen de disco de destino donde se combinarán las imágenes de disco seleccionadas.

</dd> <dt>

*newDiskImageType* \[ En\]
</dt> <dd>

Tipo de nueva imagen de disco de destino. Los tipos de imagen permitidos para la nueva imagen de disco de destino son **vmDiskType \_ Dynamic** y **vmDiskType \_ FixedSize.** Para más información, consulte [**VMHardDiskType.**](vmharddisktype.md)

</dd> <dt>

*mergeTask* \[ out, retval\]
</dt> <dd>

Objeto [**IVMTask que**](ivmtask.md) se usa para realizar un seguimiento de la finalización del proceso de combinación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                                    | La operación se realizó correctamente.<br/>                                                                                                                                                                                                                                                                      |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                      | Un parámetro es **NULL.**<br/>                                                                                                                                                                                                                                                                           |
| <dl> <dt>**E \_ InvalidarG**</dt> <dt>0x80000003</dt> </dl>                                   | El *parámetro newDiskImagePath* está vacío.<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ARCHIVO DE ERROR \_ \_ NO \_ ENCONTRADO)**</dt> <dt>0X80070002</dt> </dl>   | El sistema no puede encontrar el archivo especificado por el *parámetro newDiskImagePath.*<br/>                                                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(RUTA DE ACCESO DE ERROR \_ \_ NO \_ ENCONTRADA)**</dt> <dt>0X80070003</dt> </dl>   | El sistema no puede encontrar la ruta de acceso especificada por el *parámetro newDiskImagePath.*<br/>                                                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ NOMBRE NO \_ VÁLIDO)**</dt> <dt>0x8007007b</dt> </dl>      | El *parámetro newDiskImagePath* contiene un carácter no válido (uno de los siguientes: " \* ?<>/ \| ":").<br/>                                                                                                                                                                                         |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>      | El *parámetro newDiskImagePath* especifica una ruta de acceso vacía o relativa. Se requiere una ruta de acceso absoluta.<br/>                                                                                                                                                                                                |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl>   | La ruta de acceso especificada por el *parámetro newDiskImagePath* es demasiado larga. La ruta de acceso debe tener menos de 260 caracteres.<br/>                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(INFRACCIÓN \_ DE USO COMPARTIDO DE \_ ERRORES)**</dt> <dt>0x80070020</dt> </dl> | El disco duro virtual al que hace referencia este objeto está en uso o el elemento primario de este disco duro virtual está en uso.<br/>                                                                                                                                                                                |
| <dl> <dt>**Máquina virtual \_ E \_ ERROR DE TIPO DE \_ \_ \_ IMAGEN**</dt> <dt>DE HD 0xA004067B</dt> </dl>                   | Este error se debe a que la imagen de disco duro virtual a la que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) no es una imagen de disco de diferenciación o porque el parámetro *newDiskImageType* no es uno de los valores aceptados, **vmDiskType \_ Dynamic** o **vmDiskType \_ FixedSize.**<br/> |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ YA \_ EXISTE)**</dt> <dt>0X800700B7</dt> </dl>    | El archivo al que hace referencia el *parámetro newDiskImagePath* ya existe.<br/>                                                                                                                                                                                                                            |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ DISK \_ FULL)**</dt> <dt>0x80070070</dt> </dl>         | El volumen del host no tiene suficiente espacio para combinar este disco duro virtual.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**Máquina virtual \_ E \_ RUTA DE ACCESO PRIMARIA NO \_ \_ \_ ENCONTRADA**</dt> <dt>0XA0040677</dt> </dl>                 | El elemento primario del disco duro virtual al que hace referencia este objeto no existe.<br/>                                                                                                                                                                                                                      |
| <dl> <dt>**Máquina virtual \_ E \_ APP \_ SHUTTING \_ DOWN**</dt> <dt>0xA0040209</dt> </dl>                      | La imagen de disco duro virtual no se puede combinar porque la aplicación se está cerrando.<br/>                                                                                                                                                                                                             |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                              | Se produjo un error inesperado.<br/>                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

