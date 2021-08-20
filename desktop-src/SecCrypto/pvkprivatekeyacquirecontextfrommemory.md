---
description: Crea un contenedor temporal en el proveedor de servicios criptográficos (CSP) y carga una clave privada de la memoria en el contenedor.
ms.assetid: 9388b49b-fad4-4499-a391-fe58ed672552
title: Función PvkPrivateKeyAcquireContextFromMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeyAcquireContextFromMemory
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 3f22e6135fbad3ed4919ec44620f5b1234f17b21c27b0a3048848d258adabbd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117975869"
---
# <a name="pvkprivatekeyacquirecontextfrommemory-function"></a>Función PvkPrivateKeyAcquireContextFromMemory

> [!IMPORTANT]
> Esta API está en desuso. Microsoft puede quitar esta API en futuras versiones.

 

La **función PvkPrivateKeyAcquireContextFromMemory** crea un contenedor temporal en el [](../secgloss/p-gly.md) proveedor de servicios criptográficos [*(CSP)*](../secgloss/c-gly.md) y carga una clave privada de la memoria en el contenedor.

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI PvkPrivateKeyAcquireContextFromMemory(
  _In_        LPCWSTR    pwszProvName,
  _In_        DWORD      dwProvType,
  _In_        BYTE       *pbData,
  _In_        DWORD      cbData,
  _In_        HWND       hwndOwner,
  _In_        LPCWSTR    pwszKeyName,
  _Inout_opt_ DWORD      *pdwKeySpec,
  _Out_       HCRYPTPROV *phCryptProv,
  _Out_       LPTSTR     *ppwszTmpContainer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszProvName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene el nombre del CSP cuyo tipo se solicita en *dwProvType*.

</dd> <dt>

*dwProvType* \[ En\]
</dt> <dd>

Valor **DWORD** para el tipo CSP. Para obtener más información sobre los tipos de CSP, vea [Tipos de proveedor de servicios criptográficos](cryptographic-provider-types.md).

</dd> <dt>

*pbData* \[ En\]
</dt> <dd>

Puntero a un búfer para recibir los datos de contexto. El autor de la llamada debe proporcionar este recurso.

</dd> <dt>

*cbData* \[ En\]
</dt> <dd>

Valor **DWORD** que especifica el tamaño, en bytes, del *búfer pbData.* El autor de la llamada debe proporcionar este valor.

</dd> <dt>

*hwndOwner* \[ En\]
</dt> <dd>

Si se requiere una contraseña para descifrar los datos de contexto a los que apunta el parámetro *pbData,* este parámetro es un identificador para el elemento primario del cuadro de diálogo; de lo contrario, es **NULL.**

</dd> <dt>

*pwszKeyName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene el nombre de la clave que se recuperará.

</dd> <dt>

*pdwKeySpec* \[ in, out, optional\]
</dt> <dd>

Puntero a un **valor DWORD** que especifica el tipo de clave. Los valores posibles **incluyen AT \_ KEYEXCHANGE** o **AT \_ SIGNATURE.**

</dd> <dt>

*phCryptProv* \[ out\]
</dt> <dd>

Puntero a un identificador para el CSP.

</dd> <dt>

*ppwszTmpContainer* \[ out\]
</dt> <dd>

Dirección de un puntero a una cadena terminada en NULL para el nombre del contenedor temporal. La **función PvkPrivateKeyAcquireContextFromMemory** proporciona el búfer para esta cadena y la inicializa. Al llamar **a PvkPrivateKeyAcquireContextFromMemory**, la dirección debe apuntar a un **valor NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ha hecho correctamente, esta función devuelve **TRUE.** La **función PvkPrivateKeyAcquireContextFromMemory** devuelve **FALSE** si se produce un error.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
