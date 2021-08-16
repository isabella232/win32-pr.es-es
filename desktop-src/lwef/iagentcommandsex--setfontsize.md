---
title: IAgentCommandsEx SetFontSize
description: IAgentCommandsEx SetFontSize
ms.assetid: 095f78d2-ef91-4880-ad49-dd9a94f02891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92319178f2fbceb7b2e0cad9bdb35b740ebeaf108f864edb84b4413353e85e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477207"
---
# <a name="iagentcommandsexsetfontsize"></a>IAgentCommandsEx::SetFontSize

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in character's pop-up menu
);
```

Establece el tamaño de la fuente que se muestra en el menú emergente del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*
</dt> <dd>

Tamaño de la fuente.

</dd> </dl>

Esta propiedad determina el tamaño de punto de la fuente utilizada para mostrar texto en el menú emergente del carácter cuando la aplicación cliente está activa en la entrada. El valor predeterminado de la configuración de fuente se basa en la configuración de fuente del menú para la configuración del identificador de idioma del carácter o, si no se establece, la configuración de idioma predeterminada del usuario. Si no es input-active, [](/windows/desktop/lwef/the-command-object) [](caption-property.md) el texto del título de comando de la aplicación cliente aparece en el tamaño de punto especificado para el cliente activo de entrada.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx::GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx::GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md)


 

 