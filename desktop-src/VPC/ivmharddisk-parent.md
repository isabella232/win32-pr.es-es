---
title: Propiedad primaria IVMHardDisk (VPCCOMInterfaces. h)
description: Primario del disco duro virtual de diferenciación.
ms.assetid: 9a400fa0-ee0d-4474-a410-82756ea544fe
keywords:
- Propiedad principal de PC virtual
- Propiedad primaria Virtual PC, interfaz IVMHardDisk
- Interfaz IVMHardDisk Virtual PC, propiedad principal
topic_type:
- apiref
api_name:
- IVMHardDisk.Parent
- IVMHardDisk.get_Parent
- IVMHardDisk.put_Parent
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9487750b67fc133f4b15f15050a74638f3d0f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995899"
---
# <a name="ivmharddiskparent-property"></a>IVMHardDisk::P propiedad Princip

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera y establece el elemento primario del disco duro virtual de diferenciación.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Parent(
  [in]          IVMHardDisk *parent
);

HRESULT get_Parent(
  [out, retval] IVMHardDisk **parent
);
```



## <a name="property-value"></a>Valor de propiedad

Establece el objeto [**IVMHardDisk**](ivmharddisk.md) asociado a la imagen del disco duro principal.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                                                                                                                                                                                                              |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                                    | El parámetro es **null**.<br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>S \_ FALSO</dt> <dt>1</dt> </dl>                                               | No se trata de un disco duro de diferenciación, por lo que no tiene ningún elemento primario.<br/>                                                                                                                                                                                                                 |
| <dl> <dt>HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)</dt> <dt>0x80070002</dt> </dl> | El sistema no encontró el archivo del disco duro virtual principal.<br/>                                                                                                                                                                                                               |
| <dl> <dt>HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)</dt> <dt>0x80070003</dt> </dl> | El sistema no encontró la ruta de acceso al archivo de disco duro virtual principal.<br/>                                                                                                                                                                                                   |
| <dl> <dt>Máquina virtual \_ E \_ HD \_ Image \_ Open \_ FAIL</dt> <dt>0xA004067C</dt> </dl>                  | Se produjo un error al intentar abrir el archivo de imagen de disco duro actual.<br/>                                                                                                                                                                                               |
| <dl> <dt>Máquina virtual \_ E 0xA0040681 de \_ \_ \_ acceso a imágenes HD</dt> <dt></dt> </dl>                      | Error al intentar obtener acceso al archivo de imagen de disco duro actual.<br/>                                                                                                                                                                                             |
| <dl> <dt>Máquina virtual \_ Error \_ de \_ \_ \_ coincidencia de ID. de elemento secundario E</dt> <dt>0xA0040685</dt> </dl>            | La imagen del disco duro virtual que se encuentra en el parámetro *primario* no tiene el mismo identificador que la imagen de disco secundaria. Asegúrese de que la imagen del disco duro virtual principal que se encuentra en el parámetro *principal* es la misma que se usa para crear la imagen de disco duro virtual de diferenciación.<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Observaciones

Esta propiedad solo es válida con imágenes de disco duro de diferenciación.

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

 

