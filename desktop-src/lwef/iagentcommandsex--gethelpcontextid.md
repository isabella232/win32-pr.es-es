---
title: IAgentCommandsEx GetHelpContextID
description: IAgentCommandsEx GetHelpContextID
ms.assetid: db5f93e9-8cd3-4147-94b4-50cfe12033c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a49a633a66622626973e450b9566033b1ad96e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077670"
---
# <a name="iagentcommandsexgethelpcontextid"></a><span data-ttu-id="c3efe-103">IAgentCommandsEx::GetHelpContextID</span><span class="sxs-lookup"><span data-stu-id="c3efe-103">IAgentCommandsEx::GetHelpContextID</span></span>

<span data-ttu-id="c3efe-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c3efe-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of Commands object help topic ID
);
```

<span data-ttu-id="c3efe-105">Recupera [**HelpContextID**](helpcontextid-property.md) para un objeto [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="c3efe-105">Retrieves the [**HelpContextID**](helpcontextid-property.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="c3efe-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c3efe-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c3efe-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*</span><span class="sxs-lookup"><span data-stu-id="c3efe-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="c3efe-108">Dirección de una variable que recibe el número de contexto del tema de ayuda para el objeto de [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="c3efe-108">Address of a variable that receives the context number of the help topic for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

</dd> </dl>

<span data-ttu-id="c3efe-109">Si ha creado un archivo de ayuda de Windows para la aplicación y ha establecido la propiedad [**HelpFile**](helpfile-property.md) del carácter, Microsoft Agent llama automáticamente a Help cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **true** y el usuario selecciona el objeto de [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="c3efe-109">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects your [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="c3efe-110">Si hay un número de contexto en el [**HelpContextID**](helpcontextid-property.md), el agente llama a help y busca el tema identificado por el número de contexto actual.</span><span class="sxs-lookup"><span data-stu-id="c3efe-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="c3efe-111">El número de contexto actual es el valor de **HelpContextID** para el objeto de **comando** .</span><span class="sxs-lookup"><span data-stu-id="c3efe-111">The current context number is the value of **HelpContextID** for the **Command** object.</span></span>

<span data-ttu-id="c3efe-112">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="c3efe-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="c3efe-113">La compilación de un archivo de ayuda requiere el compilador de ayuda de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c3efe-113">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="c3efe-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c3efe-114">See Also</span></span>

<span data-ttu-id="c3efe-115">[**IAgentCommandsEx:: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="c3efe-115">[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 