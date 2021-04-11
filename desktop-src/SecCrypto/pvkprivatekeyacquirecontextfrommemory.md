---
description: Crea un contenedor temporal en el proveedor de servicios criptográficos (CSP) y carga una clave privada de la memoria en el contenedor.
ms.assetid: 9388b49b-fad4-4499-a391-fe58ed672552
title: PvkPrivateKeyAcquireContextFromMemory función)
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
ms.openlocfilehash: 1552d1e35845ffb7407d11d6e520b914ab805d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361296"
---
# <a name="pvkprivatekeyacquirecontextfrommemory-function"></a>PvkPrivateKeyAcquireContextFromMemory función)

> [!IMPORTANT]
> Esta API está en desuso. Microsoft puede quitar esta API en futuras versiones.

 

La función **PvkPrivateKeyAcquireContextFromMemory** crea un contenedor temporal en el [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) y carga una [*clave privada*](../secgloss/p-gly.md) de la memoria en el contenedor.

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

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

*pwszProvName* \[ de\]
</dt> <dd>

Un puntero a una cadena terminada en null que contiene el nombre del CSP cuyo tipo se solicita en *dwProvType*.

</dd> <dt>

*dwProvType* \[ de\]
</dt> <dd>

Valor **DWORD** para el tipo de CSP. Para obtener más información sobre los tipos de CSP, consulte [tipos de proveedor de servicios criptográficos](cryptographic-provider-types.md).

</dd> <dt>

*pbData* \[ de\]
</dt> <dd>

Un puntero a un búfer para recibir los datos de contexto. El autor de la llamada debe proporcionar este recurso.

</dd> <dt>

*cbData* \[ de\]
</dt> <dd>

Valor **DWORD** que especifica el tamaño, en bytes, del búfer *pbData* . El autor de la llamada debe proporcionar este valor.

</dd> <dt>

*hwndOwner* \[ de\]
</dt> <dd>

Si se requiere una contraseña para descifrar los datos de contexto a los que apunta el parámetro *pbData* , este parámetro es un identificador del elemento primario del cuadro de diálogo. de lo contrario, es **null**.

</dd> <dt>

*pwszKeyName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que contiene el nombre de la clave que se va a recuperar.

</dd> <dt>

*pdwKeySpec* \[ in, out, opcional\]
</dt> <dd>

Un puntero a un valor **DWORD** que especifica el tipo de clave. Entre los valores posibles se incluyen **en \_ KEYEXCHANGE** o **en la \_ signatura**.

</dd> <dt>

*phCryptProv* \[ enuncia\]
</dt> <dd>

Un puntero a un identificador para el CSP.

</dd> <dt>

*ppwszTmpContainer* \[ enuncia\]
</dt> <dd>

Dirección de un puntero a una cadena terminada en null para el nombre del contenedor temporal. La función **PvkPrivateKeyAcquireContextFromMemory** proporciona el búfer para esta cadena y lo inicializa. Al llamar a **PvkPrivateKeyAcquireContextFromMemory**, la dirección debe apuntar a un valor **null** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cuando se realiza correctamente, esta función devuelve **true**. La función **PvkPrivateKeyAcquireContextFromMemory** devuelve **false** si se produce un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
