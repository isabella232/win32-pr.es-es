---
description: Comprueba la firma de un archivo firmado y obtiene el valor hash y el identificador del algoritmo para el archivo.
ms.assetid: 130b3c3e-cc67-44ec-acc7-daa87b714299
title: Función WTHelperGetFileHash
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476350"
---
# <a name="wthelpergetfilehash-function"></a>Función WTHelperGetFileHash

\[La **función WTHelperGetFileHash** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

La **función WTHelperGetFileHash** comprueba la firma de un archivo firmado y obtiene el valor hash y el identificador del algoritmo para el archivo.

> [!Note]  
> Esta función no se declara en un archivo de encabezado publicado. Para usar esta función, declare en el formato exacto que se muestra. Esta función tampoco tiene ninguna biblioteca de importación asociada. Debe usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Wintrust.dll.

 

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

*pwszFilename* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode terminada en NULL que contiene la ruta de acceso y el nombre de archivo del archivo para el que se obtiene el hash.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este parámetro no se usa y debe ser cero.

</dd> <dt>

*pvReserved* \[ in, out, optional\]
</dt> <dd>

Este parámetro no se usa y debe ser **NULL.**

</dd> <dt>

*pbFileHash* \[ out, opcional\]
</dt> <dd>

Puntero a un búfer para recibir el valor hash del archivo. El *parámetro kbFileHash* contiene el tamaño de este búfer.

</dd> <dt>

*pwFileHash* \[ in, out, optional\]
</dt> <dd>

Puntero a una variable **DWORD** que, en la entrada, contiene el tamaño, en bytes, del búfer *pbFileHash* y, en la salida, recibe el tamaño, en bytes, del valor hash.

Para obtener el tamaño necesario del valor hash, pase **NULL para** el *parámetro pbFileHash.* Esta función colocará el tamaño necesario, en bytes, del valor hash en esta ubicación.

Si el *parámetro pbFileHash* no es **NULL** y el tamaño no es lo suficientemente grande como para recibir el valor hash, esta función colocará el tamaño necesario, en bytes, en esta ubicación y devolverá **ERROR MORE \_ \_ DATA**.

</dd> <dt>

*pHashAlgid* \[ out, opcional\]
</dt> <dd>

Puntero a una variable [**de \_ identificador de ALG**](alg-id.md) para recibir el identificador del algoritmo utilizado para crear el valor hash. Este parámetro puede ser **NULL** si no se necesita esta información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un código de estado que indica el éxito o el error de la función.

Los códigos de retorno posibles incluyen, entre otros, los siguientes.



| Código devuelto                                                                                               | Descripción                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ CORRECTO**</dt> </dl>             | El archivo está firmado y se ha comprobado la firma.<br/>                                                                                        |
| <dl> <dt>**ERROR \_ MÁS \_ DATOS**</dt> </dl>          | El *parámetro pbFileHash* no es **NULL** y el tamaño especificado por el *parámetrofileFileHash* no es lo suficientemente grande como para recibir el hash.<br/> |
| <dl> <dt>**ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**</dt> </dl> | Error de asignación de memoria.<br/>                                                                                                      |
| <dl> <dt>**TRUST \_ E \_ BAD \_ DIGEST**</dt> </dl>      | No se comprobó la firma del archivo.<br/>                                                                                                |
| <dl> <dt>**TRUST \_ E \_ NOSIGNATURE**</dt> </dl>      | El archivo no estaba firmado o tenía una firma que no es válida.<br/>                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



 

 
