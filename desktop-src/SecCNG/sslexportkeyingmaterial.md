---
description: Exporta material de creación de claves según el estándar RFC 5705.
ms.assetid: 19624852-B1A6-4BB4-96AF-0457834DA294
title: Función SslExportKeyingMaterial (Sslprovider. h)
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
ms.openlocfilehash: 906a7535b297f309c0c8471843ce07f43a110a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818499"
---
# <a name="sslexportkeyingmaterial-function"></a>SslExportKeyingMaterial función)

Exporta material de creación de claves según el [estándar RFC 5705](https://tools.ietf.org/html/rfc5705). Esta función usa la función pseudoaleatorios de TLS para generar un búfer de bytes de material de creación de claves. Toma una referencia al secreto principal, la etiqueta ASCII ambigüedad, los valores aleatorios de cliente y servidor y, opcionalmente, los datos de contexto de la aplicación.

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

*hSslProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor del protocolo TLS.

</dd> <dt>

*hMasterKey* \[ de\]
</dt> <dd>

Identificador del objeto de clave maestra que se utilizará para crear el material de creación de claves para br exportado.

</dd> <dt>

*sLabel* \[ de\]
</dt> <dd>

una cadena de etiqueta ASCII terminada en NULL. Schannel quitará el carácter NUL de terminación antes de pasarlo a la función pseudoaleatorios.

</dd> <dt>

*pbRandoms* \[ de\]
</dt> <dd>

Un puntero a un búfer que contiene una concatenación de los valores aleatorios de *cliente \_* y de *servidor \_* de la conexión TLS.

</dd> <dt>

*cbRandoms* \[ de\]
</dt> <dd>

La longitud, en bytes, del búfer *pbRandoms* .

</dd> <dt>

*pbContextValue* \[ en, opcional\]
</dt> <dd>

Un puntero a un búfer que contiene el contexto de la aplicación. Si *pbContextValue* es **null**, *cbContextValue* debe ser cero.

</dd> <dt>

*cbContextValue* \[ de\]
</dt> <dd>

La longitud, en bytes, del búfer *pbContextValue* .

</dd> <dt>

*pbOutput* \[ enuncia\]
</dt> <dd>

La dirección de un búfer que recibe el material de creación de claves exportado. El parámetro *cbOutput* contiene el tamaño de este búfer. Este valor no puede ser **null**.

</dd> <dt>

*cbOutput* \[ de\]
</dt> <dd>

La longitud, en bytes, del búfer *pbOutput* . Debe ser mayor que cero.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

No se utiliza. Debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, lo siguiente.



| Código o valor devuelto                                                                                                                                                    | Descripción                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt> </dl> | Uno de los identificadores proporcionados no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 




