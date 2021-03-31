---
description: Obtiene un identificador para un proveedor de servicios criptográficos (CSP) basado en un archivo de clave privada o un nombre de contenedor de claves.
ms.assetid: 82cdaa6f-e747-4c9d-8d2d-5fa206891eed
title: PvkGetCryptProv función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkGetCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 026b31d021dc6ff2569ad9ce8f17d2e7f0d17b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913618"
---
# <a name="pvkgetcryptprov-function"></a>PvkGetCryptProv función)

> [!IMPORTANT]
> Esta API está en desuso. Microsoft puede quitar esta API en futuras versiones.

 

La función **PvkGetCryptProv** obtiene un identificador de un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) basado en un archivo de [*clave privada*](../secgloss/p-gly.md) o un nombre de contenedor de claves.

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI PvkGetCryptProv(
  _In_      HWND       hwnd,
  _In_      LPCWSTR    pwszCaption,
  _In_      LPCWSTR    pwszCapiProvider,
  _In_      DWORD      dwProviderType,
  _In_      LPCWSTR    pwszPvkFile,
  _In_      LPCWSTR    pwszKeyContainerName,
  _Out_     DWORD      *pdwKeySpec,
  _Out_opt_ LPWSTR     *ppwszTmpContainer,
  _Out_     HCRYPTPROV *phCryptProv
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWnd* \[ de\]
</dt> <dd>

Si se requiere una contraseña para descifrar el archivo de clave privada, este parámetro es un identificador del cuadro de diálogo de contraseña principal. de lo contrario, es **null**.

</dd> <dt>

*pwszCaption* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null para la leyenda del cuadro de diálogo.

</dd> <dt>

*pwszCapiProvider* \[ de\]
</dt> <dd>

Un puntero a una cadena terminada en null para el nombre de CSP.

</dd> <dt>

*dwProviderType* \[ de\]
</dt> <dd>

Valor **DWORD** que representa el tipo de proveedor de servicios criptográficos. Para obtener más información, vea [tipos de proveedor de servicios criptográficos](cryptographic-provider-types.md).

</dd> <dt>

*pwszPvkFile* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que contiene el nombre de un archivo de clave privada.

</dd> <dt>

*pwszKeyContainerName* \[ de\]
</dt> <dd>

Un puntero a una cadena terminada en null para el nombre del contenedor de claves privadas.

</dd> <dt>

*pdwKeySpec* \[ enuncia\]
</dt> <dd>

Un puntero a un valor **DWORD** para el tipo de clave del contenedor devuelto con *phCryptProv* y *ppwszTmpContainer*.

</dd> <dt>

*ppwszTmpContainer* \[ out, opcional\]
</dt> <dd>

Dirección de un puntero a una cadena terminada en null para el nombre del contenedor de claves temporal. La función **PvkGetCryptProv** proporciona e inicializa el contenedor temporal. Al llamar a **PvkGetCryptProv**, la dirección debe apuntar a un valor **null** .

</dd> <dt>

*phCryptProv* \[ enuncia\]
</dt> <dd>

Un puntero a un identificador para el CSP.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve **S \_ correcto**.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

## <a name="remarks"></a>Observaciones

La función **PvkGetCryptProv** primero intenta obtener el identificador de proveedor desde el nombre del contenedor de claves especificado por el parámetro *pwszKeyContainerName* . Si pasa **null** para el parámetro *pwszKeyContainerName* , **PvkGetCryptProv** intenta obtener el proveedor del archivo de clave privada especificado en el parámetro *pwszPvkFile* .

Cuando haya terminado de usar el CSP, libere el identificador del proveedor y el contenedor de claves temporal mediante una llamada a la función [**PvkFreeCryptProv**](pvkfreecryptprov.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
