---
description: Exporta el material de clave según el estándar RFC 5705.
ms.assetid: 19624852-B1A6-4BB4-96AF-0457834DA294
title: Función SslExportKeyingMaterial (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKeyingMaterial
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 39aaebba64f92794e179af95a5a175e2603fccc40410989cfcd427c6a7a1a88e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906623"
---
# <a name="sslexportkeyingmaterial-function"></a>Función SslExportKeyingMaterial

Exporta el material de clave según [el estándar RFC 5705.](https://tools.ietf.org/html/rfc5705) Esta función usa la función seudoaleativo TLS para generar un búfer de bytes de material de clave. Toma una referencia al secreto maestro, la etiqueta ASCII de eliminación de ambigüedad, los valores aleatorios de cliente y servidor y, opcionalmente, los datos de contexto de la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslExportKeyingMaterial(
  _In_     NCRYPT_PROV_HANDLE hSslProvider,
  _In_     NCRYPT_KEY_HANDLE  hMasterKey,
  _In_     PCHAR              sLabel,
  _In_     PBYTE              pbRandoms,
  _In_     DWORD              cbRandoms,
  _In_opt_ PBYTE              pbContextValue,
  _In_     WORD               cbContextValue,
  _Out_    PBYTE              pbOutput,
  _In_     DWORD              cbOutput,
  _In_     DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ En\]
</dt> <dd>

Identificador de la instancia del proveedor de protocolo TLS.

</dd> <dt>

*hMasterKey* \[ En\]
</dt> <dd>

Identificador del objeto de clave maestra que se usará para crear el material de clave que se va a exportar.

</dd> <dt>

*sLabel* \[ En\]
</dt> <dd>

una cadena de etiqueta ASCII terminada en NUL. Schannel quitará el carácter NUL de terminación antes de pasarlo a la función pseudoaleativo.

</dd> <dt>

*pbRandoms* \[ En\]
</dt> <dd>

Puntero a un búfer que contiene *una \_* concatenación de los valores aleatorios de cliente y *aleatorios \_* del servidor de la conexión TLS.

</dd> <dt>

*cbRandoms* \[ En\]
</dt> <dd>

Longitud, en bytes, del *búfer pbRandoms.*

</dd> <dt>

*pbContextValue* \[ en, opcional\]
</dt> <dd>

Puntero a un búfer que contiene el contexto de la aplicación. Si *pbContextValue* es **NULL,** *cbContextValue* debe ser cero.

</dd> <dt>

*cbContextValue* \[ En\]
</dt> <dd>

Longitud, en bytes, del *búfer pbContextValue.*

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Dirección de un búfer que recibe el material de clave exportado. El *parámetro cbOutput* contiene el tamaño de este búfer. Este valor no puede ser **NULL.**

</dd> <dt>

*cbOutput* \[ En\]
</dt> <dd>

Longitud, en bytes, del *búfer pbOutput.* Debe ser mayor que cero.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

No se usa. Debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, los siguientes.



| Código o valor devuelto                                                                                                                                                    | Descripción                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ IDENTIFICADOR \_ NO VÁLIDO**</dt> <dt>0x80090026L</dt> </dl> | Uno de los identificadores proporcionados no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 




