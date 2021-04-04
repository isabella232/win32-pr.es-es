---
title: IAgentCharacterEx GetSRModeID
description: IAgentCharacterEx GetSRModeID
ms.assetid: 28049680-8245-49f3-9ecd-13c7605f10ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0bba237fb1bc1b5d769f7e8ecf983b58718c18e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "103788998"
---
# <a name="iagentcharacterexgetsrmodeid"></a><span data-ttu-id="0a766-103">IAgentCharacterEx::GetSRModeID</span><span class="sxs-lookup"><span data-stu-id="0a766-103">IAgentCharacterEx::GetSRModeID</span></span>

<span data-ttu-id="0a766-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0a766-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSRModeID(
   BSTR * pbszModeID  // address of speech recognition engine ID
);
```

<span data-ttu-id="0a766-105">Recupera el identificador de modo del conjunto de motores de reconocimiento de voz para el carácter.</span><span class="sxs-lookup"><span data-stu-id="0a766-105">Retrieves the mode ID of the speech recognition engine set for the character.</span></span>

-   <span data-ttu-id="0a766-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0a766-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0a766-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span><span class="sxs-lookup"><span data-stu-id="0a766-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="0a766-108">Dirección de un BSTR que recibe la configuración de ID. de modo del motor de reconocimiento de voz para el carácter.</span><span class="sxs-lookup"><span data-stu-id="0a766-108">Address of a BSTR that receives the mode ID setting of the speech recognition engine for the character.</span></span>

</dd> </dl>

<span data-ttu-id="0a766-109">Esta configuración devuelve el conjunto de motores para la entrada de voz de un carácter.</span><span class="sxs-lookup"><span data-stu-id="0a766-109">This setting returns the engine set for a character's speech input.</span></span> <span data-ttu-id="0a766-110">El identificador de modo de un motor de reconocimiento de voz es una representación de cadena del GUID (con formato de llaves y guiones) por parte del proveedor de voz que identifica el motor de forma exclusiva.</span><span class="sxs-lookup"><span data-stu-id="0a766-110">The mode ID for a speech recognition engine is a string representation of the GUID (formatted with braces and dashes) by the speech vendor uniquely identifying the engine.</span></span> <span data-ttu-id="0a766-111">Para obtener más información, consulte la [documentación del SDK de Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="0a766-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="0a766-112">Si no establece un identificador de modo de motor de reconocimiento de voz para el carácter, el servidor devuelve un motor que coincide con la configuración de idioma del carácter (mediante interfaces de Microsoft Speech API).</span><span class="sxs-lookup"><span data-stu-id="0a766-112">If you do not set a speech recognition engine mode ID for the character, the server returns an engine that matches the character's language setting (using Microsoft Speech API interfaces).</span></span> <span data-ttu-id="0a766-113">Si no hay ningún motor de reconocimiento de voz coincidente disponible para el carácter, el servidor devuelve una cadena nula (vacía).</span><span class="sxs-lookup"><span data-stu-id="0a766-113">If there is no matching speech recognition engine available for the character, the server returns a null (empty) string.</span></span>

<span data-ttu-id="0a766-114">Cuando se habilita la entrada de voz (en la ventana Opciones de caracteres avanzadas), al consultar o establecer esta propiedad se cargará el motor asociado (si aún no está cargado) y se iniciarán los servicios de voz.</span><span class="sxs-lookup"><span data-stu-id="0a766-114">When speech input is enabled (in the Advanced Character Options window), querying or setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="0a766-115">Es decir, la clave de escucha está disponible y la sugerencia de escucha es visible.</span><span class="sxs-lookup"><span data-stu-id="0a766-115">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="0a766-116">(La clave de escucha y la sugerencia de escucha solo están habilitadas si también están habilitadas en opciones de caracteres avanzadas). Sin embargo, si consulta la propiedad cuando la voz está deshabilitada, el servidor no inicia Speech Services y devuelve una cadena nula (cadena vacía).</span><span class="sxs-lookup"><span data-stu-id="0a766-116">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services and it returns a null string (empty string).</span></span>

<span data-ttu-id="0a766-117">Esta función solo devuelve el valor del uso de la aplicación cliente del carácter; la configuración no refleja otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="0a766-117">This function returns only the setting for your client application's use of the character; the setting does not reflect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="0a766-118">Esta función no genera un error si [**IAgentSpeechInputProperties:: GetEnabled**](iagentspeechinputproperties--getenabled.md) devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="0a766-118">This function does not fail if the [**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**.</span></span>

<span data-ttu-id="0a766-119">Los requisitos del motor de voz de Microsoft Agent se basan en Microsoft Speech API.</span><span class="sxs-lookup"><span data-stu-id="0a766-119">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="0a766-120">Los motores que admiten los requisitos de SAPI de Microsoft Agent se pueden instalar y usar con el agente.</span><span class="sxs-lookup"><span data-stu-id="0a766-120">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a766-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0a766-121">See Also</span></span>

[<span data-ttu-id="0a766-122">**IAgentCharacterEx::SetSRModeID**</span><span class="sxs-lookup"><span data-stu-id="0a766-122">**IAgentCharacterEx::SetSRModeID**</span></span>](iagentcharacterex--setsrmodeid.md)


 

 




