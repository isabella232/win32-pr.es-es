---
title: Método IVMVirtualPC GetHardDisk (VPCCOMInterfaces.h)
description: Recupera un objeto correspondiente a un archivo de imagen de disco existente.
ms.assetid: 648a3f8a-5114-4c14-b9a9-f175941333ab
keywords:
- Equipo virtual del método GetHardDisk
- Método GetHardDisk Virtual PC , interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , método GetHardDisk
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
ms.openlocfilehash: bc57085662c62951032837db178888bac5cb4407b11d7777d2f165f7b9c5a100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136588"
---
# <a name="ivmvirtualpcgetharddisk-method"></a>IVMVirtualPC::GetHardDisk (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

*imagePath* \[ En\]
</dt> <dd>

Ruta de acceso completa a un archivo de imagen de disco existente.

</dd> <dt>

*hardDisk* \[ out, retval\]
</dt> <dd>

Objeto [**IVMHardDisk**](ivmharddisk.md) correspondiente a esta imagen de disco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                                                         |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                    | El *parámetro imagePath* *o hardDisk* es **NULL.**<br/>                                                                  |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32 (ARCHIVO DE ERROR \_ \_ NO \_ ENCONTRADO)**</dt> <dt>0X80070002</dt> </dl> | El sistema no puede encontrar el archivo especificado por el *parámetro imagePath.*<br/>                                               |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32 (RUTA DE ACCESO DE ERROR \_ \_ NO \_ ENCONTRADA)**</dt> <dt>0X80070003</dt> </dl> | El sistema no puede encontrar la ruta de acceso especificada por el *parámetro imagePath.*<br/>                                               |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ INVALID \_ NAME) 0X8007007B**</dt> <dt></dt> </dl>    | El *parámetro imagePath* contiene un carácter no válido (uno de " \* ?:<>/ \| "").<br/>                                  |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0X800700A1</dt> </dl>    | El *parámetro imagePath* especifica una ruta de acceso vacía o relativa. Se requiere una ruta de acceso absoluta.<br/>                          |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | La ruta de acceso especificada por el *parámetro imagePath* es demasiado larga. La longitud de la ruta de acceso debe tener menos de 260 caracteres.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                     |
| <dl> <dt>**Máquina virtual \_ E \_ HARDWARE \_ VIRTUALIZATION \_ DISABLED**</dt> <dt>0xA0040951</dt> </dl>     | El procesador no admite extensiones de Virtualización acelerada por hardware (HAV).<br/>                                  |



 

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

 

