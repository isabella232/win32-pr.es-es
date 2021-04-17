---
description: Descarga la firma del archivo. cab, comprueba los permisos asociados a los paquetes y los ejecuta según la autenticación.
ms.assetid: b86a8f39-73a1-4e17-ac83-9ed095de4922
title: DownloadJavaEX función)
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
ms.openlocfilehash: 31371e91599d604db591ee3e921b42bc809aae21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660656"
---
# <a name="downloadjavaex-function"></a>DownloadJavaEX función)

Descarga la firma del archivo. cab, comprueba los permisos asociados a los paquetes y los ejecuta según la autenticación.

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

*Reservado* \[ de\]
</dt> <dd>

Este parámetro está reservado.

</dd> <dt>

*pProviderData* \[ de\]
</dt> <dd>

Una estructura de [**\_ \_ datos del proveedor de cifrado**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) que contiene los datos del certificado, como los permisos de archivo y de zona.

</dd> <dt>

*pJava* \[ de\]
</dt> <dd>

Estructura [**del \_ \_ proveedor de directivas de Java**](/previous-versions//bb432350(v=vs.85)) que contiene los datos relacionados con el proveedor de directivas.

</dd> <dt>

*pFunctions* \[ de\]
</dt> <dd>

Una estructura de [**\_ \_ funciones de proveedor de cifrado**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) que contiene una lista de métodos para comprobar objetos de certificado, firmas y directivas finales.

</dd> <dt>

*fCertificate* \[ de\]
</dt> <dd>

Si hay un certificado, este parámetro es **true**. De lo contrario, es **false**.

</dd> <dt>

*pTrust* \[ de\]
</dt> <dd>

Una estructura de [**\_ confianza de Java**](/windows/desktop/api/Capi/ns-capi-java_trust) que contiene información de confianza como el permiso codificado, la firma del codificador y el código de la Directiva de devolución auténtica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**. De lo contrario, el valor devuelto es un código de error.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Javacypt.dll</dt> </dl> |



 

 
