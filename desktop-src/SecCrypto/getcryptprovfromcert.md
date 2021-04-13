---
description: Obtiene un identificador para un proveedor de servicios criptográficos (CSP) y una especificación de clave para un contexto de certificado.
ms.assetid: ff72231f-e10f-49d2-b0e0-0008923803cc
title: GetCryptProvFromCert función)
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
ms.openlocfilehash: bcd396c45333dee42bae4cb8bdfdd52792f1bdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361624"
---
# <a name="getcryptprovfromcert-function"></a>GetCryptProvFromCert función)

> [!IMPORTANT]
> Esta API está en desuso. Microsoft puede quitar esta API en futuras versiones.

 

La función **GetCryptProvFromCert** obtiene un identificador a un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) y una especificación de clave para un contexto de [*certificado*](../secgloss/c-gly.md) . Utilice esta función para obtener acceso a la [*clave privada*](../secgloss/p-gly.md) del emisor del certificado.

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

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

*hWnd* \[ de\]
</dt> <dd>

Identificador de la ventana que se va a usar como propietario de los cuadros de diálogo que se muestran. Este miembro no se utiliza actualmente y se omite. Es seguro pasar **null** para este parámetro.

</dd> <dt>

*pCert* \[ de\]
</dt> <dd>

Puntero a una estructura [**de \_ contexto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) de certificado para el certificado.

</dd> <dt>

*phCryptProv* \[ enuncia\]
</dt> <dd>

Puntero a una estructura [**HCRYPTPROV**](hcryptprov.md) que es un identificador para el CSP.

</dd> <dt>

*pdwKeySpec* \[ enuncia\]
</dt> <dd>

Especificación de la clave privada que se va a recuperar. Entre los valores posibles se incluyen **en \_ KEYEXCHANGE** o **en la \_ signatura**.

</dd> <dt>

*pfDidCryptAcquire* \[ de\]
</dt> <dd>

Valor que especifica si la función adquirió el identificador del proveedor basándose en el certificado.

</dd> <dt>

*ppwszTmpContainer* \[ out, opcional\]
</dt> <dd>

Dirección de un puntero a una cadena terminada en null para el nombre del contenedor de claves temporal. La función **GetCryptProvFromCert** proporciona e inicializa el contenedor temporal. Al llamar a **GetCryptProvFromCert**, la dirección debe apuntar a un valor **null** .

</dd> <dt>

*ppwszProviderName* \[ out, opcional\]
</dt> <dd>

Dirección de un puntero a una cadena terminada en null para el nombre del proveedor. La función **GetCryptProvFromCert** devuelve el nombre del proveedor. Al llamar a **GetCryptProvFromCert**, la dirección debe apuntar a un valor **null** .

</dd> <dt>

*pdwProviderType* \[ enuncia\]
</dt> <dd>

Especifica el tipo de CSP. Puede ser cero o uno de los [tipos de proveedor de servicios criptográficos](cryptographic-provider-types.md). Si este miembro es cero, el contenedor de claves es uno de los proveedores de almacenamiento de claves CNG.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cuando se realiza correctamente, esta función devuelve **true**. La función **GetCryptProvFromCert** devuelve **false** si se produce un error.

## <a name="remarks"></a>Observaciones

La herramienta [Makecert](makecert.md) llama a **GetCryptProvFromCert** cuando se invoca mediante la opción **de línea de comandos-is** .

Si el parámetro *pfDidCryptAcquire* se establece en **true**, la función establece los parámetros *phCryptProv*, *pdwKeySpec* y *pdwProviderType* en los valores del proveedor.

Cuando haya terminado de usar el CSP, libere el servicio llamando a la función [**FreeCryptProvFromCert**](freecryptprovfromcert.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
