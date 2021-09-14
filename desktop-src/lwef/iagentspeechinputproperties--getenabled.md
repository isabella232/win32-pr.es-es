---
title: IAgentSpeechInputProperties GetEnabled
description: IAgentSpeechInputProperties GetEnabled
ms.assetid: 5731f9ad-eb2e-4a79-a724-b3c263235c8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c95613398bf79b2446d2bc572864f69ad1ad92ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358972"
---
# <a name="iagentspeechinputpropertiesgetenabled"></a>IAgentSpeechInputProperties::GetEnabled

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of variable for speech recognition engine 
);                   // Enabled setting
```

Recupera un valor que indica si el motor de reconocimiento de voz instalado está habilitado.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

Dirección de una variable que recibe **True si** el motor de voz está habilitado actualmente y **False** si está deshabilitado.

</dd> </dl>

 

 




