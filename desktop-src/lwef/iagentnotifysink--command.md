---
title: IAgentNotifySink (comando)
description: IAgentNotifySink (comando)
ms.assetid: d54fb2e8-27d6-47a4-8a1e-5419a94ea26d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d9c20de96c1bb14cf003ad7beff98e716e272ad3de39532d9b455e279d97af3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105220"
---
# <a name="iagentnotifysinkcommand"></a>IAgentNotifySink::Command

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Command(
   long dwCommandID,         // Command ID of the best match
   IUnknown * punkUserInput  // address of IAgentUserInput object 
);                          
```

Notifica a una aplicación cliente que [**el usuario**](/windows/desktop/lwef/the-command-object) seleccionó un comando.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

Identificador de la mejor alternativa de comando de coincidencia.

</dd> <dt>

<span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*userUserInput*
</dt> <dd>

Dirección de la [**interfaz IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) para el [**objeto IAgentUserInput.**](iagentuserinput.md)

</dd> </dl>

Use [**QueryInterface para**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) recuperar la [**interfaz IAgentUserInput.**](iagentuserinput.md)

El servidor notifica al cliente activo de entrada cuando el usuario elige un comando por voz o seleccionando un comando en el menú emergente del carácter. El evento tiene lugar incluso cuando el usuario selecciona uno de los comandos del servidor. En este caso, el servidor devuelve un identificador de comando null, la puntuación de confianza y el texto de voz devuelto por el motor de voz para esa entrada.

## <a name="see-also"></a>Consulte también

[**IAgentUserInput**](iagentuserinput.md)


 

 