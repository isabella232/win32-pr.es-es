---
description: Un mensaje de terminación se envía inmediatamente después de un mensaje de especificación de cifrado de cambios para comprobar que los procesos de intercambio de claves y autenticación se realizaron correctamente.
ms.assetid: 1ae92223-3729-48be-af42-146c9cbae6a5
title: Finalizar mensajes en el protocolo TLS 1.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e9af7502f0865661e2ed0f6a80059cb822395002ccaf035373dc3db322adac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006983"
---
# <a name="finish-messages-in-the-tls-10-protocol"></a>Finalizar mensajes en el protocolo TLS 1.0

Un mensaje de terminación se envía inmediatamente después de un mensaje de especificación de cifrado de cambios para comprobar que los procesos de intercambio de claves y autenticación se realizaron correctamente. Los mensajes finales del protocolo TLS 1.0 se calculan mediante la función [*pseudo*](../secgloss/p-gly.md) aleatoria (PRF) con la clave maestra [*,*](../secgloss/m-gly.md)una etiqueta y un valor de ed como entrada. PRF genera una salida de longitud arbitraria. El método siguiente se usa para generar la salida de PRF usada en los mensajes de fin de TLS 1.0.

Se genera un [*identificador hash*](../secgloss/h-gly.md) PRF mediante [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) con el valor de ID de **ALG \_** establecido en CALG TLS1PRF y el identificador de la clave maestra pasada en el \_ parámetro *hKey.* Los valores de etiqueta y valor de valor de ed se establecen en el identificador hash mediante los valores HP TLS1PRF LABEL y HP TLS1PRF SEED, respectivamente, en el parámetro dwParam con la función \_ \_ \_ \_ [**CryptSetHashParam.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam)  Por último, el motor de protocolo llama a la función [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) con el valor HP HASHVAL en el parámetro \_ *dwParam* para recuperar los datos PRF que se incluirán en el mensaje de fin. Al realizar la llamada a **CryptGetHashParam,** el motor de protocolo debe especificar cuántos bytes de datos prF se producirán. Esto se hace en el *parámetro pdwDataLen* y los datos resultantes se colocan en el búfer al que apunta el *parámetro pbData.*

A continuación se muestra un código fuente típico para este motor de protocolo:


```C++
CRYPT_DATA_BLOB Data;
HCRYPTHASH hFinishHash;
BYTE rgbFinishPRF[12];
BYTE rgbCliHashOfHandshakes[36];

//------------------------------------------------------------
// get client finish message

CryptCreateHash(
         hProv, 
         CALG_TLS1PRF, 
         hMasterKey, 
         0, 
         &hFinishHash);

Data.pbData = (BYTE*)"client finished";
Data.cbData = 15;
CryptSetHashParam(
         hFinishHash, 
         HP_TLS1PRF_LABEL, 
         (BYTE*)&Data, 
         0);

Data.pbData = rgbCliHashOfHandshakes;
Data.cbData = sizeof(rgbCliHashOfHandshakes);
CryptSetHashParam(
          hFinishHash, 
          HP_TLS1PRF_SEED, 
          (BYTE*)&Data, 
          0);

cbFinishPRF = sizeof(rgbFinishPRF);
CryptGetHashParam(
          hFinishHash, 
          HP_HASHVAL, 
          rgbFinishPRF, 
          &cbFinishPRF, 
          0);

CryptDestroyHash(hFinishHash);
```



 

 
