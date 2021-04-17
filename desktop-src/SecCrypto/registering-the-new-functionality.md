---
description: La compatibilidad con el registro de la nueva funcionalidad en un registro del sistema se debe proporcionar en el nuevo archivo DLL junto con la nueva función.
ms.assetid: 7a6af325-4891-40db-8d33-c9782bd438e5
title: Registrar la nueva funcionalidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470541ed9b832ad5eaa914c1a35805dbd861a843
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688422"
---
# <a name="registering-the-new-functionality"></a>Registrar la nueva funcionalidad

La compatibilidad con el registro de la nueva funcionalidad en un registro del sistema se debe proporcionar en el nuevo archivo DLL junto con la nueva función. [Las funciones de compatibilidad con OID](cryptography-functions.md) proporcionan ayuda con este registro. Regsvr32.exe registra nuevas funciones. Esta herramienta se incluye con Windows.

El nuevo archivo DLL debe proporcionar puntos de entrada de [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) para su uso por Regsvr32.exe. Las funciones [*CryptoAPI*](../secgloss/c-gly.md) , como [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) o [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction), se pueden usar dentro de estos puntos de entrada, tal como se muestra en el ejemplo siguiente.


```C++
//  The DllRegisterServer Entry Point
STDAPI DllRegisterServer(void)
{
    if(!CryptRegisterOIDFunction(
         X509_ASN_ENCODING,                  // Encoding type
         CRYPT_OID_ENCODE_OBJECT_FUNC,       // Function name
         szOID_NEW_CERTIFICATE_TYPE,         // OID
         L"NewCert.dll",                     // Dll name
         L"NewCertificateTypeEncodeObject"   // Override function
         ))                                  //   name
       {
         return E_FAIL;
       }
    else
       {
         return S_OK;
       }
}

// The DllUnregisterServer Entry Point
STDAPI DllUnregisterServer(void)
{
    HRESULT     hr = S_OK;

    if(!CryptUnregisterOIDFunction(
          X509_ASN_ENCODING,             // Encoding type
          CRYPT_OID_ENCODE_OBJECT_FUNC,  // Function name
          szOID_NEW_CERTIFICATE_TYPE     // OID
          ))
    {
       if(ERROR_FILE_NOT_FOUND != GetLastError())
               hr = E_FAIL;
    }
    return hr;
}
```



Este ejemplo se debe compilar y vincular en el nuevo archivo DLL. Estos dos puntos de entrada, junto con el punto de entrada de la función, se deben exportar.

Para instalar la nueva funcionalidad en un equipo, ejecute Regsvr32.exe desde un símbolo del sistema, especificando el nombre y la ruta de acceso del nuevo archivo DLL. Regsvr32.exe tiene acceso a la función [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) a través del punto de entrada de la función [**DllRegisterServer**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85)) y registra la nueva función y dll.

 

 
