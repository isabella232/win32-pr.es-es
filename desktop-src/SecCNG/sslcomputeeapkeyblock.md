---
description: Calcula el bloque de claves utilizado por el protocolo de autenticación extensible (EAP).
ms.assetid: 0f382668-6fc6-440f-ba61-70b1db0f3987
title: Función SslComputeEapKeyBlock (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeEapKeyBlock
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: d46c1284b208975126067ff295507b51def9133b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666961"
---
# <a name="sslcomputeeapkeyblock-function"></a>SslComputeEapKeyBlock función)

La función **SslComputeEapKeyBlock** calcula el bloque de claves que usa el protocolo de autenticación extensible (EAP).

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslComputeEapKeyBlock(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hMasterKey,
  _In_      PBYTE              pbRandoms,
  _In_      DWORD              cbRandoms,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*hMasterKey* \[ de\]
</dt> <dd>

Identificador del objeto de [*clave maestra*](/windows/desktop/SecGloss/m-gly) .

</dd> <dt>

*pbRandoms* \[ de\]
</dt> <dd>

Un puntero a un búfer que contiene una concatenación de los valores aleatorios de cliente \_ y \_ de servidor de la sesión SSL.

</dd> <dt>

*cbRandoms* \[ de\]
</dt> <dd>

La longitud, en bytes, del búfer *pbRandoms* .

</dd> <dt>

*pbOutput* \[ out, opcional\]
</dt> <dd>

La dirección de un búfer que recibe el BLOB de clave. El parámetro *cbOutput* contiene el tamaño de este búfer. Si este parámetro es **null**, esta función colocará el tamaño necesario, en bytes, en el **valor DWORD** al que apunta el parámetro *pcbResult* .

</dd> <dt>

*cbOutput* \[ de\]
</dt> <dd>

La longitud, en bytes, del búfer *pbOutput* .

</dd> <dt>

*pcbResult* \[ enuncia\]
</dt> <dd>

Un puntero a un valor **DWORD** que especifica la longitud, en bytes, del hash escrito en el búfer de *pbOutput* .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Establezca en **\_ marca de \_ servidor \_ SSL NCRYPT** para indicar que se trata de una llamada de servidor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.



| Código o valor devuelto                                                                                                                                                    | Descripción                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt> </dl> | Uno de los identificadores proporcionados no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

