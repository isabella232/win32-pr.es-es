---
description: Obtiene un identificador para un proveedor de servicios criptográficos (CSP) basado en un archivo de clave privada o un nombre de contenedor de claves.
ms.assetid: 82cdaa6f-e747-4c9d-8d2d-5fa206891eed
title: Función PvkGetCryptProv
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
ms.openlocfilehash: 5ba60ca31bf75e355126484608bfe9650b00fea60eaf876022e2de2bf5030470
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901325"
---
# <a name="pvkgetcryptprov-function"></a>Función PvkGetCryptProv

> [!IMPORTANT]
> Esta API está en desuso. Microsoft puede quitar esta API en futuras versiones.

 

La **función PvkGetCryptProv** obtiene un identificador para un proveedor [](../secgloss/p-gly.md) de servicios criptográficos [*(CSP)*](../secgloss/c-gly.md) basado en un archivo de clave privada o un nombre de contenedor de claves.

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

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

*hwnd* \[ En\]
</dt> <dd>

Si se requiere una contraseña para descifrar el archivo de clave privada, este parámetro es un identificador para el elemento primario del cuadro de diálogo de contraseña. de lo contrario, es **NULL.**

</dd> <dt>

*pwszCaption* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL para el título del cuadro de diálogo.

</dd> <dt>

*pwszCapiProvider* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL para el nombre de CSP.

</dd> <dt>

*dwProviderType* \[ En\]
</dt> <dd>

Valor **DWORD que** representa el tipo de proveedor criptográfico. Para obtener más información, vea [Tipos de proveedor de servicios criptográficos.](cryptographic-provider-types.md)

</dd> <dt>

*pwszPvkFile* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene el nombre de un archivo de clave privada.

</dd> <dt>

*pwszKeyContainerName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL para el nombre del contenedor de claves privadas.

</dd> <dt>

*pdwKeySpec* \[ out\]
</dt> <dd>

Puntero a un **valor DWORD** para el tipo de clave del contenedor devuelto con *phCryptProv* y *ppwszTmpContainer*.

</dd> <dt>

*ppwszTmpContainer* \[ out, opcional\]
</dt> <dd>

Dirección de un puntero a una cadena terminada en NULL para el nombre del contenedor de claves temporal. La **función PvkGetCryptProv** proporciona e inicializa el contenedor temporal. Al llamar **a PvkGetCryptProv,** la dirección debe apuntar a un **valor** NULL.

</dd> <dt>

*phCryptProv* \[ out\]
</dt> <dd>

Puntero a un identificador para el CSP.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **S \_ OK**.

Si se produce un error en el método, devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

## <a name="remarks"></a>Observaciones

La **función PvkGetCryptProv** intenta primero obtener el identificador del proveedor del nombre del contenedor de claves especificado por el *parámetro pwszKeyContainerName.* Si pasa **NULL para** el parámetro *pwszKeyContainerName,* **PvkGetCryptProv** intenta obtener el proveedor del archivo de clave privada especificado en el *parámetro pwszPvkFile.*

Cuando haya terminado de usar el CSP, libera el identificador del proveedor y el contenedor de claves temporales mediante una llamada a la [**función PvkFreeCryptProv.**](pvkfreecryptprov.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
