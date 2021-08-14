---
description: Comprueba un único archivo de catálogo mediante la directiva de firma de código de sistema operativo estándar, como la firma de controladores.
ms.assetid: 1e2a18a5-506e-46a8-9309-666bec92182d
title: Función pSetupVerifyCatalogFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupVerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 5c7ad6e866fd82773ab55e57011e14c1cfae2dd47d6f5c91a772eab9cfce42c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386235"
---
# <a name="psetupverifycatalogfile-function"></a>Función pSetupVerifyCatalogFile

\[Microsoft ya no admite esta función. Para un archivo INF (instalación del dispositivo), los desarrolladores deben usar **SetupVerifyInfFile**. Para validar un catálogo no basado en INF, use **WinVerifyTrust**.\]

Comprueba un único archivo de catálogo mediante la directiva de firma de código de sistema operativo estándar, como la firma de controladores.

## <a name="syntax"></a>Sintaxis


```C++
DWORD pSetupVerifyCatalogFile(
  _In_ LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CatalogFullPath* \[ En\]
</dt> <dd>

Ruta de acceso completa del archivo de catálogo que se va a comprobar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve **ERROR \_ SUCCESS;** de lo contrario, devuelve el error de [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SetupVerifyInfFile**](/windows/win32/api/setupapi/nf-setupapi-setupverifyinffilea)
</dt> <dt>

[**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)
</dt> </dl>

 

 
