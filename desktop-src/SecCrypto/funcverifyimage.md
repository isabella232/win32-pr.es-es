---
description: Lo utiliza un proveedor de servicios criptográficos (CSP) para comprobar la firma de un archivo DLL.
ms.assetid: 477a6c9f-05ac-485a-8b27-5605fc11c1d6
title: CRYPT_VERIFY_IMAGE puntero a función (Cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_VERIFY_IMAGE
- CRYPT_VERIFY_IMAGE_A
- CRYPT_VERIFY_IMAGE_W
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: e95414d09a7869aa4a2ef512fcff2765ba4491bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687598"
---
# <a name="crypt_verify_image-function-pointer"></a>CIFRAr \_ comprobar \_ puntero de función de imagen

Un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) utiliza la función de devolución de llamada **FuncVerifyImage** para comprobar la firma de un archivo dll.

Todas las DLL auxiliares en las que un CSP realiza llamadas a funciones deben estar firmadas de la misma manera (y con la misma clave) que la DLL de CSP principal. Para garantizar esta firma, los archivos dll auxiliares se deben cargar dinámicamente mediante la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) . Pero antes de que se cargue el archivo DLL, se debe comprobar la firma de la DLL. El CSP realiza esta comprobación mediante una llamada a la función **FuncVerifyImage** , tal como se muestra en el ejemplo siguiente.

## <a name="syntax"></a>Sintaxis


```C++
typedef BOOL ( WINAPI *CRYPT_VERIFY_IMAGE)(
  _In_       LPCTSTR lpszImage,
  _In_ const BYTE    *pbSigData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszImage* \[ de\]
</dt> <dd>

Dirección de una cadena terminada en null que contiene la ruta de acceso y el nombre de archivo del archivo DLL para el que se va a comprobar la firma.

</dd> <dt>

*pbSigData* \[ de\]
</dt> <dd>

Dirección de un búfer que contiene la firma.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si la función se ejecuta correctamente, **false** si se produce un error.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo usar la función de devolución de llamada **FuncVerifyImage** para comprobar la firma de un archivo dll antes de que lo cargue un CSP.


```C++
BOOL (FARPROC *ProvVerifyImage)(LPCSTR lpszImage, BYTE *pSigData);


//  "ProvVerifyImage" has been set to "pVTable->FuncVerifyImage"
//  within the CPAcquireContext function.

//  bSignature is a previously assigned BYTE array that contains the
//  signature that is stored in the C:\Winnt40\System32\signature.sig
//  file. During development, this file is created with the 
//  Sign.exe tool.
...


//  Verify the signature in the
//  C:\Winnt40\System32\Signature.dll file.
if(RCRYPT_FAILED(ProvVerifyImage
    ("c:\\winnt40\\system32\\signature.dll",
        bSignature)) {
    SetLastError(NTE_BAD_SIGNATURE);
    return CRYPT_FAILED;
}

//  Load the DLL with the LoadLibrary function, then acquire pointers 
//  to the functions with the GetProcAddress function.
//...
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Cspdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**VTableProvStruc**](vtableprovstruc.md)
</dt> </dl>

 

 
