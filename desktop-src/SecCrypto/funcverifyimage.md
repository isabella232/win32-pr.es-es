---
description: Lo usa un proveedor de servicios criptográficos (CSP) para comprobar la firma de un archivo DLL.
ms.assetid: 477a6c9f-05ac-485a-8b27-5605fc11c1d6
title: CRYPT_VERIFY_IMAGE puntero de función (Cspdk.h)
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
ms.openlocfilehash: b33e6e627c87840e4adb7615f7e3ca5932a7402a3b3ae7110be51c0847a5f67f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006683"
---
# <a name="crypt_verify_image-function-pointer"></a>Puntero de \_ función CRYPT VERIFY \_ IMAGE

Un proveedor de servicios criptográficos [*(CSP)*](../secgloss/c-gly.md) usa la función de devolución de llamada **FuncVerifyImage** para comprobar la firma de un archivo DLL.

Todos los archivos DLL auxiliares en los que un CSP realiza llamadas de función deben firmarse de la misma manera (y con la misma clave) que el archivo DLL de CSP principal. Para garantizar esta firma, los archivos DLL auxiliares se deben cargar dinámicamente mediante la [**función LoadLibrary.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) Pero antes de cargar el archivo DLL, se debe comprobar la firma del archivo DLL. El CSP realiza esta comprobación mediante una llamada a la **función FuncVerifyImage,** como se muestra en el ejemplo siguiente.

## <a name="syntax"></a>Sintaxis


```C++
typedef BOOL ( WINAPI *CRYPT_VERIFY_IMAGE)(
  _In_       LPCTSTR lpszImage,
  _In_ const BYTE    *pbSigData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszImage* \[ En\]
</dt> <dd>

Dirección de una cadena terminada en NULL que contiene la ruta de acceso y el nombre de archivo del archivo DLL para el que se comprobará la firma.

</dd> <dt>

*pbSigData* \[ En\]
</dt> <dd>

Dirección de un búfer que contiene la firma.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si la función se realiza **correctamente, FALSE** si se produce un error.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo usar la función de devolución de llamada **FuncVerifyImage** para comprobar la firma de un archivo DLL antes de que lo cargue un CSP.


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
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Cspdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**VTableProvStruc**](vtableprovstruc.md)
</dt> </dl>

 

 
