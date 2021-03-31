---
title: Método de reflexión
description: Método de reflexión
ms.assetid: a188dd47-6af1-429d-af0a-69451f6b495e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a896c499e11aeaf50bfe9adc82a8330e61fc693
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904557"
---
# <a name="think-method"></a><span data-ttu-id="2e297-103">Método de reflexión</span><span class="sxs-lookup"><span data-stu-id="2e297-103">Think Method</span></span>

<span data-ttu-id="2e297-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2e297-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2e297-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="2e297-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2e297-106">Muestra el texto especificado para el carácter especificado en un globo de palabra "pensamiento".</span><span class="sxs-lookup"><span data-stu-id="2e297-106">Displays the specified text for the specified character in a "thought" word balloon.</span></span>

</dd> <dt>

<span data-ttu-id="2e297-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="2e297-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2e297-108">\*agente ***. Caracteres ("*** CharacterID \* *").* \*  \[ *Texto* de reflexión\]</span><span class="sxs-lookup"><span data-stu-id="2e297-108">*agent ***.Characters ("*** CharacterID\*\*\*").Think*\* \[*Text*\]</span></span>



| <span data-ttu-id="2e297-109">Parte</span><span class="sxs-lookup"><span data-stu-id="2e297-109">Part</span></span>   | <span data-ttu-id="2e297-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e297-110">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="2e297-111">*Texto*</span><span class="sxs-lookup"><span data-stu-id="2e297-111">*Text*</span></span> | <span data-ttu-id="2e297-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2e297-112">Optional.</span></span> <span data-ttu-id="2e297-113">Cadena que especifica la salida de pensamiento del carácter.</span><span class="sxs-lookup"><span data-stu-id="2e297-113">A string that specifies the character's thought output.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e297-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e297-114">Remarks</span></span>

<span data-ttu-id="2e297-115">Al igual que el método [**Speak**](speak-method.md) , el método de **reflexión** es una solicitud en cola que muestra texto en un globo de palabras, con la salvedad de que el globo de palabras de **reflexión** difiere visualmente.</span><span class="sxs-lookup"><span data-stu-id="2e297-115">Like the [**Speak**](speak-method.md) method, the **Think** method is a queued request that displays text in a word balloon, except that the **Think** word balloon differs visually.</span></span> <span data-ttu-id="2e297-116">Además, el globo solo admite la etiqueta de control de voz de marcador (**\\ MRK**) y omite cualquier otra etiqueta de control de voz.</span><span class="sxs-lookup"><span data-stu-id="2e297-116">In addition, the balloon supports only the Bookmark speech control tag (**\\Mrk**) and ignores any other speech control tags.</span></span> <span data-ttu-id="2e297-117">A diferencia de **Speak**, el método de **reflexión** no cambia el estado de animación del carácter.</span><span class="sxs-lookup"><span data-stu-id="2e297-117">Unlike **Speak**, the **Think** method does not change the character's animation state.</span></span>

<span data-ttu-id="2e297-118">Las propiedades del objeto [**Balloon**](/windows/desktop/lwef/the-balloon-object) afectan a la salida de los métodos [**Speak**](speak-method.md) y **opina** .</span><span class="sxs-lookup"><span data-stu-id="2e297-118">The [**Balloon**](/windows/desktop/lwef/the-balloon-object) object's properties affect the output of both the [**Speak**](speak-method.md) and **Think** methods.</span></span> <span data-ttu-id="2e297-119">Por ejemplo, la propiedad [**Enabled**](enabled-property.md) del objeto **Balloon** debe ser **true** para que el texto se muestre.</span><span class="sxs-lookup"><span data-stu-id="2e297-119">For example, the **Balloon** object's [**Enabled**](enabled-property.md) property must be **True** for text to display.</span></span>

<span data-ttu-id="2e297-120">Si declara una referencia de objeto y la establece en este método, devuelve un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="2e297-120">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="2e297-121">Además, si no se ha cargado el archivo, el servidor establece la propiedad [**status**](status-property.md) del objeto **request** en "Failed" con un número de código de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="2e297-121">In addition, if the file has not been loaded, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error code number.</span></span>

<span data-ttu-id="2e297-122">La separación de palabras automática del agente en el globo de palabras rompe las palabras mediante caracteres de espacio en blanco (por ejemplo, espacio o tabulación).</span><span class="sxs-lookup"><span data-stu-id="2e297-122">Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, Space or Tab).</span></span> <span data-ttu-id="2e297-123">Sin embargo, si no es posible, puede romper una palabra para ajustarse al globo.</span><span class="sxs-lookup"><span data-stu-id="2e297-123">However, if it cannot, it may break a word to fit the balloon.</span></span> <span data-ttu-id="2e297-124">En idiomas como el japonés, el chino y el tailandés, en los que no se usan espacios para romper palabras, inserte un carácter de espacio de cero (0x200B) de Unicode entre caracteres para definir saltos de palabra lógicos.</span><span class="sxs-lookup"><span data-stu-id="2e297-124">In languages like Japanese, Chinese, and Thai where spaces are not used to break words, insert a Unicode zero-width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="2e297-125">Establezca el identificador de idioma del carácter antes de usar el método [**Speak**](speak-method.md) para asegurarse de que el texto se muestre correctamente en el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="2e297-125">Set the character's language ID before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

 

 