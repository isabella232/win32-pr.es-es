---
description: Obtiene el tamaño de un certificado para un controlador de pantalla.
ms.assetid: fd52e939-127a-4493-8406-31f7767921cd
title: GetCertificateSize función)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360090"
---
# <a name="getcertificatesize-function"></a>GetCertificateSize función)

> [!IMPORTANT]
> El administrador de protección de [salida](output-protection-manager.md) (OPM) usa esta función para tener acceso a la funcionalidad del controlador de pantalla. Las aplicaciones no deben llamar a esta función.

 

Obtiene el tamaño de un certificado para un controlador de pantalla.

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

*pstrDeviceName* \[ de\]
</dt> <dd>

Puntero a una estructura de [**\_ cadena Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) que contiene el nombre del dispositivo de pantalla, tal y como lo devuelve la función [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .

</dd> <dt>

*ctPVPCertificateType* \[ de\]
</dt> <dd>

El tipo de certificado, especificado como miembro de la enumeración del **\_ \_ tipo de certificado DXGKMDT** .

</dd> <dt>

*pulCertificateLength* \[ enuncia\]
</dt> <dd>

Recibe el tamaño del certificado, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**. De lo contrario, devuelve un código de error **NTSTATUS** .

## <a name="remarks"></a>Observaciones

Las aplicaciones deben llamar al método [**IOPMVideoOutput:: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) en lugar de esta función.

Esta función no tiene ninguna biblioteca de importación asociada. Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de OPM](opm-functions.md)
</dt> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> </dl>

 

 
