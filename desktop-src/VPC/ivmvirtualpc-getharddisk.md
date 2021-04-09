---
title: Método IVMVirtualPC GetHardDisk (VPCCOMInterfaces. h)
description: Recupera un objeto correspondiente a un archivo de imagen de disco existente.
ms.assetid: 648a3f8a-5114-4c14-b9a9-f175941333ab
keywords:
- Método GetHardDisk Virtual PC
- Método GetHardDisk Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método GetHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 558d098b6745718830c63dd700c14febf4f6bed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996874"
---
# <a name="ivmvirtualpcgetharddisk-method"></a>IVMVirtualPC:: GetHardDisk (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera un objeto correspondiente a un archivo de imagen de disco existente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetHardDisk(
  [in]          BSTR        imagePath,
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*imagePath* \[ de\]
</dt> <dd>

Ruta de acceso completa a un archivo de imagen de disco existente.

</dd> <dt>

disco *duro* \[ out, retval\]
</dt> <dd>

Objeto [**IVMHardDisk**](ivmharddisk.md) correspondiente a esta imagen de disco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                                                         |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                    | El parámetro *imagePath* o disco *duro* es **null**.<br/>                                                                  |
| <dl> <dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)**</dt> <dt>0x80070002</dt> </dl> | El sistema no encuentra el archivo especificado por el parámetro *imagePath* .<br/>                                               |
| <dl> <dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt> </dl> | El sistema no puede encontrar la ruta de acceso especificada por el parámetro *imagePath* .<br/>                                               |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt> </dl>    | El parámetro *imagePath* contiene un carácter no válido (uno de " \* ?: <>/ \| " ").<br/>                                  |
| <dl> <dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt> </dl>    | El parámetro *imagePath* especifica una ruta de acceso relativa o vacía. Se requiere una ruta de acceso absoluta.<br/>                          |
| <dl> <dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt> </dl> | La ruta de acceso especificada por el parámetro *imagePath* es demasiado larga. La longitud de la ruta de acceso debe ser inferior a 260 caracteres.<br/> |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                     |
| <dl> <dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt> </dl>     | El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).<br/>                                  |



 

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

 

