---
title: Método IVMFstonepyDrive AttachImage (VPCCOMInterfaces.h)
description: Adjunta una imagen de disquete del host a la unidad de disquete de la máquina virtual.
ms.assetid: ee7ea6ac-47ef-4e7b-8df3-28c716a728b0
keywords:
- Pc virtual del método AttachImage
- Método AttachImage De PC virtual, interfaz IVMFstonepyDrive
- IVMFstonepyDrive interface Virtual PC , método AttachImage
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21af305d0e7441fc931765795bb4e5d0785a211af6806ee80fd679d6f487b218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595719"
---
# <a name="ivmfloppydriveattachimage-method"></a>IVMFstonepyDrive::AttachImage (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Adjunta una imagen de disquete del host a la unidad de disquete de la máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AttachImage(
  [in] BSTR mediaImagePath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mediaImagePath* \[ En\]
</dt> <dd>

Ruta de acceso completa a la imagen de disquete que se va a adjuntar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                                                                |
| <dl> <dt>**E \_ InvalidarG**</dt> <dt>0x80000003</dt> </dl>                                 | El *parámetro mediaImagePath* no es válido.<br/>                                                                                 |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                    | El parámetro es **NULL.**<br/>                                                                                                   |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl>      | No hay suficiente memoria disponible para completar esta solicitud.<br/>                                                               |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | La ruta de acceso especificada por el *parámetro mediaImagePath* es demasiado larga. La ruta de acceso debe tener menos de **MAX \_ PATH** (260) caracteres.<br/> |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ INVALID \_ NAME) 0X8007007B**</dt> <dt></dt> </dl>    | El *parámetro mediaImagePath* contiene un carácter no válido (uno de " \* ?<>/ \| ":").<br/>                                    |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0X800700A1</dt> </dl>    | El *parámetro mediaImagePath* especifica una ruta de acceso vacía o relativa. Se requiere una ruta de acceso absoluta.<br/>                            |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                            | La configuración de esta máquina virtual no es válida o no se encuentra.<br/>                                                  |
| <dl> <dt>**Máquina virtual \_ ERROR \_ DE CAPTURA DE IMÁGENES \_ \_ E**</dt> <dt>0xA00400650</dt> </dl>                  | No se pudo capturar el archivo de imagen especificado.<br/>                                                                              |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMFstonepyDrive se define como \_ 661abee6-112a-4ed9-tanf-3c874969f10e<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMFstonepyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

