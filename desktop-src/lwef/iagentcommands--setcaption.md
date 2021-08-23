---
title: IAgentCommands SetCaption
description: IAgentCommands SetCaption
ms.assetid: 042f7366-0071-40a5-a47c-81c02cdbe3a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b38138d218804461afc782efc14ff3685f55d2f737db6fdb21c39021efbcb36e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665475"
---
# <a name="iagentcommandssetcaption"></a>IAgentCommands::SetCaption

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Commands collection
);
```

Establece el [**texto de**](caption-property.md) título que se muestra para una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

BSTR que especifica el valor de la propiedad [**Caption**](caption-property.md) para una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> </dl>

Al establecer la propiedad [**Caption**](caption-property.md) para una colección [**Commands,**](/windows/desktop/lwef/the-commands-collection-object) se define cómo aparecerá en el menú emergente del carácter cuando su propiedad [**Visible**](visible-property.md) esté establecida en **True** y la aplicación no sea el cliente activo de entrada. Para especificar una clave de acceso (mnemotécnica sin línea) para el título **,** incluya un carácter de yerba (&) antes de ese carácter.

Si define comandos para una colección Commands que tiene su conjunto [**de**](caption-property.md) [**títulos,**](/windows/desktop/lwef/the-commands-collection-object) normalmente también se define un **título** para su **colección Commands.**

## <a name="see-also"></a>Consulte también

[**IAgentCommands::GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands::SetVisible**](iagentcommands--setvisible.md), [**IAgentCommands::SetVoice**](iagentcommands--setvoice.md)


 

 