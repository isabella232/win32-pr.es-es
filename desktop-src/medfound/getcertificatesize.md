---
description: Obtiene el tamaño de un certificado para un controlador para mostrar.
ms.assetid: fd52e939-127a-4493-8406-31f7767921cd
title: Función GetCertificateSize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateSize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: bcd1f49ce65978c6a89c89cee1fda38e41434065
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257919"
---
# <a name="getcertificatesize-function"></a>Función GetCertificateSize

> [!IMPORTANT]
> El Administrador de [](output-protection-manager.md) protección de salida (OPM) usa esta función para acceder a la funcionalidad del controlador de pantalla. Las aplicaciones no deben llamar a esta función.

 

Obtiene el tamaño de un certificado para un controlador para mostrar.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI GetCertificateSize(
  _In_  PUNICODE_STRING          pstrDeviceName,
  _In_  DXGKMDT_CERTIFICATE_TYPE ctPVPCertificateType,
  _Out_ ULONG                    *pulCertificateLength
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pstrDeviceName* \[ En\]
</dt> <dd>

Puntero a una [**estructura \_ STRING UNICODE**](/windows/win32/api/subauth/ns-subauth-unicode_string) que contiene el nombre del dispositivo para mostrar, tal y como devuelve la función [**GetMonitorInfo.**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa)

</dd> <dt>

*ctPVPCertificateType* \[ En\]
</dt> <dd>

Tipo de certificado, especificado como miembro de la **enumeración DXGKMDT \_ CERTIFICATE \_ TYPE.**

</dd> <dt>

*pulCertificateLength* \[ out\]
</dt> <dd>

Recibe el tamaño del certificado, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **STATUS \_ SUCCESS**. De lo contrario, devuelve un código de error **NTSTATUS.**

## <a name="remarks"></a>Observaciones

Las aplicaciones deben llamar [**al método IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) en lugar de esta función.

Esta función no tiene ninguna biblioteca de importación asociada. Para llamar a esta función, debe usar las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de OPM](opm-functions.md)
</dt> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> </dl>

 

 
