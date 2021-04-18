---
description: Se envía un mensaje de finalización inmediatamente después de un mensaje de especificación de cifrado de cambios para comprobar que el intercambio de claves y los procesos de autenticación se han realizado correctamente.
ms.assetid: 1ae92223-3729-48be-af42-146c9cbae6a5
title: Finalizar mensajes en el protocolo TLS 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a0f0f3e85916e66d434cb3e69b083348e40143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688192"
---
# <a name="finish-messages-in-the-tls-10-protocol"></a><span data-ttu-id="488a4-103">Finalizar mensajes en el protocolo TLS 1,0</span><span class="sxs-lookup"><span data-stu-id="488a4-103">Finish Messages in the TLS 1.0 Protocol</span></span>

<span data-ttu-id="488a4-104">Se envía un mensaje de finalización inmediatamente después de un mensaje de especificación de cifrado de cambios para comprobar que el intercambio de claves y los procesos de autenticación se han realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="488a4-104">A finish message is sent immediately after a change cipher spec message to verify the success of key exchange and authentication processes.</span></span> <span data-ttu-id="488a4-105">Los mensajes de finalización del protocolo TLS 1,0 se calculan mediante la [*función pseudoaleatorios*](../secgloss/p-gly.md) (PRF) con la [*clave maestra*](../secgloss/m-gly.md), una etiqueta y un inicialización como entrada.</span><span class="sxs-lookup"><span data-stu-id="488a4-105">The finish messages in the TLS 1.0 protocol are calculated using [*Pseudo-Random Function*](../secgloss/p-gly.md) (PRF) with the [*master key*](../secgloss/m-gly.md), a label, and a seed as input.</span></span> <span data-ttu-id="488a4-106">PRF genera una salida de longitud arbitraria.</span><span class="sxs-lookup"><span data-stu-id="488a4-106">PRF produces an output of arbitrary length.</span></span> <span data-ttu-id="488a4-107">El método siguiente se usa para generar la salida PRF usada en los mensajes de finalización TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="488a4-107">The following method is used to generate the PRF output used in TLS 1.0 finish messages.</span></span>

<span data-ttu-id="488a4-108">Un identificador de [*hash*](../secgloss/h-gly.md) PRF se genera mediante [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) con el valor de **\_ ID. de alg** establecido en CALG \_ TLS1PRF y el identificador de la clave maestra pasada en el parámetro *hKey* .</span><span class="sxs-lookup"><span data-stu-id="488a4-108">A PRF [*hash*](../secgloss/h-gly.md) handle is generated using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) with the **ALG\_ID** value set to CALG\_TLS1PRF and the handle to the master key passed in the *hKey* parameter.</span></span> <span data-ttu-id="488a4-109">Los valores de inicialización y de etiqueta se establecen en el identificador de hash usando los valores de la etiqueta HP TLS1PRF y el valor de \_ \_ inicialización de HP \_ TLS1PRF \_ , respectivamente, en el parámetro *dwParam* con la función [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) .</span><span class="sxs-lookup"><span data-stu-id="488a4-109">The label and seed values are set on the hash handle using the values HP\_TLS1PRF\_LABEL and HP\_TLS1PRF\_SEED, respectively, in the *dwParam* parameter with the [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) function.</span></span> <span data-ttu-id="488a4-110">Por último, el motor de protocolo llama a la función [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) con el valor HP \_ HASHVAL en el parámetro *dwParam* para recuperar los datos PRF que se van a incluir en el mensaje de finalización.</span><span class="sxs-lookup"><span data-stu-id="488a4-110">Finally, the protocol engine calls the function [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) with the value HP\_HASHVAL in the *dwParam* parameter to retrieve the PRF data to be included in the finish message.</span></span> <span data-ttu-id="488a4-111">Al realizar la llamada a **CryptGetHashParam**, el motor de protocolo debe especificar el número de bytes de datos que creará el PRF.</span><span class="sxs-lookup"><span data-stu-id="488a4-111">When making the call to **CryptGetHashParam**, the protocol engine must specify how many bytes of data PRF will produce.</span></span> <span data-ttu-id="488a4-112">Esto se hace en el parámetro *pdwDataLen* y los datos resultantes se colocan en el búfer señalado por el parámetro *pbData* .</span><span class="sxs-lookup"><span data-stu-id="488a4-112">This is done in the *pdwDataLen* parameter, and the resulting data is placed in the buffer pointed to by the *pbData* parameter.</span></span>

<span data-ttu-id="488a4-113">El siguiente es el código fuente típico de este motor de protocolo:</span><span class="sxs-lookup"><span data-stu-id="488a4-113">The following is typical source code for this protocol engine:</span></span>


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



 

 
