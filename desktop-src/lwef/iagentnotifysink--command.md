---
title: Comando IAgentNotifySink
description: Comando IAgentNotifySink
ms.assetid: d54fb2e8-27d6-47a4-8a1e-5419a94ea26d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690d2914db9d284cd4ba4b826905d3169b83f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995191"
---
# <a name="iagentnotifysinkcommand"></a>IAgentNotifySink:: Command

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Command(
   long dwCommandID,         // Command ID of the best match
   IUnknown * punkUserInput  // address of IAgentUserInput object 
);                          
```

Notifica a una aplicación cliente que el usuario ha seleccionado un [**comando**](/windows/desktop/lwef/the-command-object) .

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

Identificador de la alternativa del comando mejor coincidencia.

</dd> <dt>

<span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punkUserInput*
</dt> <dd>

Dirección de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) para el objeto [**IAgentUserInput**](iagentuserinput.md) .

</dd> </dl>

Use [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para recuperar la interfaz [**IAgentUserInput**](iagentuserinput.md) .

El servidor notifica al cliente de entrada-activo cuando el usuario elige un comando por voz o seleccionando un comando en el menú emergente del carácter. El evento se produce incluso cuando el usuario selecciona uno de los comandos del servidor. En este caso, el servidor devuelve un identificador de comando nulo, la puntuación de confianza y el texto de la voz que devuelve el motor de voz para esa entrada.

## <a name="see-also"></a>Consulte también

[**IAgentUserInput**](iagentuserinput.md)


 

 