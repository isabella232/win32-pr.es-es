---
description: Obtiene un identificador para un proveedor de servicios criptográficos (CSP) y una especificación de clave para un contexto de certificado.
ms.assetid: ff72231f-e10f-49d2-b0e0-0008923803cc
title: Función GetCryptProvFromCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: c885c439014a26bafba3be8614981c67d200e9f87cd4e3c4f03e8cbcc1b77e38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006663"
---
# <a name="getcryptprovfromcert-function"></a>Función GetCryptProvFromCert

> [!IMPORTANT]
> Esta API está en desuso. Microsoft puede quitar esta API en futuras versiones.

 

La **función GetCryptProvFromCert** obtiene un identificador para un proveedor de servicios criptográficos [*(CSP)*](../secgloss/c-gly.md) y una especificación de clave para un contexto [*de*](../secgloss/c-gly.md) certificado. Use esta función para obtener acceso a la [*clave privada del*](../secgloss/p-gly.md) emisor del certificado.

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI GetCryptProvFromCert(
  _In_      HWND           hwnd,
  _In_      PCCERT_CONTEXT pCert,
  _Out_     HCRYPTPROV     *phCryptProv,
  _Out_     DWORD          *pdwKeySpec,
  _In_      BOOL           *pfDidCryptAcquire,
  _Out_opt_ LPWSTR         *ppwszTmpContainer,
  _Out_opt_ LPWSTR         *ppwszProviderName,
  _Out_     DWORD          *pdwProviderType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwnd* \[ En\]
</dt> <dd>

Identificador de la ventana que se usará como propietario de los cuadros de diálogo que se muestran. Este miembro no se usa actualmente y se omite. Es seguro pasar **NULL para** este parámetro.

</dd> <dt>

*pCert* \[ En\]
</dt> <dd>

Puntero a una [**estructura CERT \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) para el certificado.

</dd> <dt>

*phCryptProv* \[ out\]
</dt> <dd>

Puntero a una [**estructura HCRYPTPROV**](hcryptprov.md) que es un identificador del CSP.

</dd> <dt>

*pdwKeySpec* \[ out\]
</dt> <dd>

Especificación de la clave privada que se recuperará. Los valores posibles **incluyen AT \_ KEYEXCHANGE** o **AT \_ SIGNATURE.**

</dd> <dt>

*pfDidCryptAcquire* \[ En\]
</dt> <dd>

Valor que especifica si la función adquirió el identificador del proveedor en función del certificado.

</dd> <dt>

*ppwszTmpContainer* \[ out, opcional\]
</dt> <dd>

Dirección de un puntero a una cadena terminada en NULL para el nombre del contenedor de claves temporales. La **función GetCryptProvFromCert** proporciona e inicializa el contenedor temporal. Al llamar **a GetCryptProvFromCert**, la dirección debe apuntar a un **valor NULL.**

</dd> <dt>

*ppwszProviderName* \[ out, opcional\]
</dt> <dd>

Dirección de un puntero a una cadena terminada en NULL para el nombre del proveedor. La **función GetCryptProvFromCert** devuelve el nombre del proveedor. Al llamar **a GetCryptProvFromCert**, la dirección debe apuntar a un **valor NULL.**

</dd> <dt>

*pdwProviderType* \[ out\]
</dt> <dd>

Especifica el tipo de CSP. Puede ser cero o uno de los tipos [de proveedor de servicios criptográficos](cryptographic-provider-types.md). Si este miembro es cero, el contenedor de claves es uno de los proveedores de almacenamiento de claves CNG.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ha hecho correctamente, esta función devuelve **TRUE.** La **función GetCryptProvFromCert** devuelve **FALSE** si se produce un error.

## <a name="remarks"></a>Comentarios

La [herramienta MakeCert](makecert.md) llama **a GetCryptProvFromCert** cuando se invoca mediante la opción de línea de comandos **-is.**

Si el *parámetro pfDidCryptAcquire* se establece en **TRUE,** la función establece los parámetros *phCryptProv*, *pdwKeySpec* y *pdwProviderType* en los valores del proveedor.

Cuando haya terminado de usar csp, descríbalo llamando a la [**función FreeCryptProvFromCert.**](freecryptprovfromcert.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
