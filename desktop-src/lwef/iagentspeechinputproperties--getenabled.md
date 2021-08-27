---
title: IAgentSpeechInputProperties GetEnabled
description: IAgentSpeechInputProperties GetEnabled
ms.assetid: 5731f9ad-eb2e-4a79-a724-b3c263235c8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404bd6f0348487c8e039c247f5a9368359133be9e3df76b884115679a2961a97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114675"
---
# <a name="iagentspeechinputpropertiesgetenabled"></a>IAgentSpeechInputProperties::GetEnabled

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

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

 

 




