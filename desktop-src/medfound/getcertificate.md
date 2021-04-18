---
description: Obtiene un certificado para un controlador de pantalla.
ms.assetid: eceaf151-1dae-4ff0-9139-7f1789f6c682
title: GetCertificate función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificate
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 30cb17345177b552e51120afd00758a3f6886584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705403"
---
# <a name="getcertificate-function"></a>GetCertificate función)

> [!IMPORTANT]
> El administrador de protección de [salida](output-protection-manager.md) (OPM) usa esta función para tener acceso a la funcionalidad del controlador de pantalla. Las aplicaciones no deben llamar a esta función.

 

Obtiene un certificado para un controlador de pantalla.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI GetCertificate(
  _In_  PUNICODE_STRING          pstrDeviceName,
  _In_  DXGKMDT_CERTIFICATE_TYPE ctPVPCertificateType,
  _Out_ BYTE                     *pbCertificate,
  _Out_ ULONG                    ulCertificateLength
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

*pbCertificate* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que recibe el certificado.

</dd> <dt>

*ulCertificateLength* \[ enuncia\]
</dt> <dd>

Tamaño del búfer de *pbCertificate* , en bytes. Para obtener el tamaño del certificado, llame a [**GetCertificateSize**](getcertificatesize.md).

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

 

 
