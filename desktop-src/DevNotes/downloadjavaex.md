---
description: Descarga la .cab de archivo, comprueba los permisos asociados a los paquetes y los ejecuta en función de la autenticación.
ms.assetid: b86a8f39-73a1-4e17-ac83-9ed095de4922
title: Función DownloadJavaEX
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownloadJavaEX
api_type:
- DllExport
api_location:
- Javacypt.dll
ms.openlocfilehash: 628fdb1b8b0ec9979d844c8f48fb02fbf8f6a642a96c925f427c868160dd6b27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795265"
---
# <a name="downloadjavaex-function"></a>Función DownloadJavaEX

Descarga la .cab de archivo, comprueba los permisos asociados a los paquetes y los ejecuta en función de la autenticación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI DownloadJavaEX(
  _In_ PALLOCATOR               Reserved,
  _In_ PCRYPT_PROVIDER_DATA     pProviderData,
  _In_ PJAVA_POLICY_PROVIDER    pJava,
  _In_ CRYPT_PROVIDER_FUNCTIONS *pFunctions,
  _In_ BOOL                     fCertificate,
  _In_ PJAVA_TRUST              pTrust
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Reservado* \[ En\]
</dt> <dd>

Este parámetro está reservado.

</dd> <dt>

*pProviderData* \[ En\]
</dt> <dd>

Estructura [**CRYPT \_ PROVIDER DATA \_ que**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) contiene datos de certificado, como permisos de archivo y zona.

</dd> <dt>

*pJava* \[ En\]
</dt> <dd>

Estructura [**JAVA POLICY PROVIDER \_ \_ que**](/previous-versions//bb432350(v=vs.85)) contiene datos relacionados con el proveedor de directivas.

</dd> <dt>

*pFunctions* \[ En\]
</dt> <dd>

Estructura [**CRYPT \_ PROVIDER \_ FUNCTIONS**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) que contiene una lista de métodos para comprobar objetos de certificado, firmas y directivas finales.

</dd> <dt>

*fCertificate* \[ En\]
</dt> <dd>

Si hay un certificado, este parámetro es **TRUE.** De lo contrario, es **FALSE.**

</dd> <dt>

*pTrust* \[ En\]
</dt> <dd>

Estructura [**TRUST \_ de JAVA**](/windows/desktop/api/Capi/ns-capi-java_trust) que contiene información de confianza, como el permiso codificado, la firma del codificador y el código de directiva de devolución auténtico.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es **S \_ OK**. De lo contrario, el valor devuelto es un código de error.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Javacypt.dll</dt> </dl> |



 

 
