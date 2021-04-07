---
description: Comprueba la firma de un archivo firmado y obtiene el valor hash y el identificador del algoritmo para el archivo.
ms.assetid: 130b3c3e-cc67-44ec-acc7-daa87b714299
title: WTHelperGetFileHash función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperGetFileHash
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 1597dfda630b1ae8cbc0d3b700b6ed9bc1a09472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002077"
---
# <a name="wthelpergetfilehash-function"></a>WTHelperGetFileHash función)

\[La función **WTHelperGetFileHash** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

La función **WTHelperGetFileHash** comprueba la firma de un archivo firmado y obtiene el valor hash y el identificador del algoritmo para el archivo.

> [!Note]  
> Esta función no se declara en un archivo de encabezado publicado. Para usar esta función, declárela en el formato exacto que se muestra. Esta función tampoco tiene asociada ninguna biblioteca de importación. Debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Wintrust.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
LONG WINAPI WTHelperGetFileHash(
  _In_        LPCWSTR pwszFilename,
  _In_        DWORD   dwFlags,
  _Inout_opt_ PVOID   pvReserved,
  _Out_opt_   BYTE    *pbFileHash,
  _Inout_opt_ DWORD   *pcbFileHash,
  _Out_opt_   ALG_ID  *pHashAlgid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszFilename* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode terminada en null que contiene la ruta de acceso y el nombre del archivo para el que se va a obtener el hash.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Este parámetro no se utiliza y debe ser cero.

</dd> <dt>

*pvReserved* \[ in, out, opcional\]
</dt> <dd>

Este parámetro no se utiliza y debe ser **null**.

</dd> <dt>

*pbFileHash* \[ out, opcional\]
</dt> <dd>

Un puntero a un búfer para recibir el valor hash del archivo. El parámetro *pcbFileHash* contiene el tamaño de este búfer.

</dd> <dt>

*pcbFileHash* \[ in, out, opcional\]
</dt> <dd>

Puntero a una variable **DWORD** que, en la entrada, contiene el tamaño, en bytes, del búfer *pbFileHash* y, en la salida, recibe el tamaño, en bytes, del valor hash.

Para obtener el tamaño requerido del valor hash, pase **null** para el parámetro *pbFileHash* . Esta función colocará el tamaño necesario, en bytes, del valor hash en esta ubicación.

Si el parámetro *pbFileHash* no es **null** y el tamaño no es lo suficientemente grande como para recibir el valor hash, esta función colocará el tamaño necesario, en bytes, en esta ubicación y devolverá los **\_ \_ datos de error**.

</dd> <dt>

*pHashAlgid* \[ out, opcional\]
</dt> <dd>

Un puntero a una variable de [**\_ identificador de alg**](alg-id.md) para recibir el identificador del algoritmo utilizado para crear el valor hash. Este parámetro puede ser **null** si no se necesita esta información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un código de estado que indica si la función se ha realizado correctamente o no.

Los códigos de retorno posibles incluyen, entre otros, lo siguiente.



| Código devuelto                                                                                               | Descripción                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ correcto**</dt> </dl>             | El archivo está firmado y se ha comprobado la firma.<br/>                                                                                        |
| <dl> <dt>**ERROR \_ más \_ datos**</dt> </dl>          | El parámetro *pbFileHash* no es **null** y el tamaño especificado por el parámetro *pcbFileHash* no es lo suficientemente grande como para recibir el hash.<br/> |
| <dl> <dt>**ERROR \_ de \_ memoria insuficiente \_**</dt> </dl> | Error de asignación de memoria.<br/>                                                                                                      |
| <dl> <dt>**CONFIANZA \_ E \_ \_ Resumen incorrecto**</dt> </dl>      | No se ha comprobado la firma del archivo.<br/>                                                                                                |
| <dl> <dt>**CONFIAR \_ E \_ nofirma**</dt> </dl>      | El archivo no estaba firmado o tenía una firma no válida.<br/>                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



 

 
