---
title: Propiedad KeyBoardLayoutStr de IMsTscAdvancedSettings
description: Especifica el nombre del identificador de configuración regional de entrada activo (anteriormente denominado distribución del teclado) que se va a usar para la conexión.
ms.assetid: a469c602-84a8-44c6-9c0f-76262961b527
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad KeyBoardLayoutStr
- Propiedad KeyBoardLayoutStr Servicios de Escritorio remoto, interfaz IMsTscAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsTscAdvancedSettings, propiedad KeyBoardLayoutStr
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.KeyBoardLayoutStr
- IMsTscAdvancedSettings.put_KeyBoardLayoutStr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4d5e6703b86f5e60a50ead05f8015df61cfdc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802276"
---
# <a name="imstscadvancedsettingskeyboardlayoutstr-property"></a><span data-ttu-id="de5ce-106">IMsTscAdvancedSettings:: KeyBoardLayoutStr (propiedad)</span><span class="sxs-lookup"><span data-stu-id="de5ce-106">IMsTscAdvancedSettings::KeyBoardLayoutStr property</span></span>

<span data-ttu-id="de5ce-107">Especifica el nombre del identificador de configuración regional de entrada activo (anteriormente denominado distribución del teclado) que se va a usar para la conexión.</span><span class="sxs-lookup"><span data-stu-id="de5ce-107">Specifies the name of the active input locale identifier (formerly called the keyboard layout) to use for the connection.</span></span>

<span data-ttu-id="de5ce-108">Si no se establece esta propiedad, el control utiliza el diseño predeterminado devuelto por la función [**GetKeyboardLayout**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) .</span><span class="sxs-lookup"><span data-stu-id="de5ce-108">If this property is not set, the control uses the default layout returned by the [**GetKeyboardLayout**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) function.</span></span>

<span data-ttu-id="de5ce-109">Esta propiedad es de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="de5ce-109">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="de5ce-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de5ce-110">Syntax</span></span>


```C++
HRESULT put_KeyBoardLayoutStr(
  [in] BSTR KeyBoardLayoutStr
);
```



## <a name="property-value"></a><span data-ttu-id="de5ce-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="de5ce-111">Property value</span></span>

<span data-ttu-id="de5ce-112">Nombre del identificador de configuración regional de entrada activo.</span><span class="sxs-lookup"><span data-stu-id="de5ce-112">The name of the active input locale identifier.</span></span>

## <a name="error-codes"></a><span data-ttu-id="de5ce-113">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="de5ce-113">Error codes</span></span>

<span data-ttu-id="de5ce-114">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="de5ce-114">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="de5ce-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de5ce-115">Remarks</span></span>

<span data-ttu-id="de5ce-116">La propiedad es un número hexadecimal de ocho dígitos en forma de cadena.</span><span class="sxs-lookup"><span data-stu-id="de5ce-116">The property is an eight digit hexadecimal number in string form.</span></span> <span data-ttu-id="de5ce-117">Los cuatro dígitos inferiores representan el identificador de idioma y los cuatro dígitos superiores representan la variación del teclado dentro de ese idioma.</span><span class="sxs-lookup"><span data-stu-id="de5ce-117">The lower four digits represent the language identifier, and the upper four digits represent the keyboard variation within that language.</span></span> <span data-ttu-id="de5ce-118">Por lo tanto, por ejemplo, "00000409" representaría el teclado inglés de EE. UU. predeterminado porque "0409" es el identificador de idioma Inglés de EE. UU.</span><span class="sxs-lookup"><span data-stu-id="de5ce-118">So, for example, "00000409" would represent the default US English keyboard because "0409" is the US English language identifier.</span></span> <span data-ttu-id="de5ce-119">La variación Dvorak del teclado inglés de EE. UU. tiene un identificador de "00010409".</span><span class="sxs-lookup"><span data-stu-id="de5ce-119">The Dvorak variation of the US English keyboard has an identifier of "00010409".</span></span> <span data-ttu-id="de5ce-120">Puede encontrar las distribuciones de teclado disponibles, enumeradas por los identificadores de distribución de teclado, en el registro en</span><span class="sxs-lookup"><span data-stu-id="de5ce-120">You can find the available keyboard layouts, listed by their keyboard layout identifiers, in the registry under</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      ControlSet001
         Control
            Keyboard Layouts
```

<span data-ttu-id="de5ce-121">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="de5ce-121">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de5ce-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de5ce-122">Requirements</span></span>



| <span data-ttu-id="de5ce-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="de5ce-123">Requirement</span></span> | <span data-ttu-id="de5ce-124">Value</span><span class="sxs-lookup"><span data-stu-id="de5ce-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="de5ce-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de5ce-125">Minimum supported client</span></span><br/> | <span data-ttu-id="de5ce-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de5ce-126">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="de5ce-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de5ce-127">Minimum supported server</span></span><br/> | <span data-ttu-id="de5ce-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de5ce-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="de5ce-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="de5ce-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="de5ce-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de5ce-130"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="de5ce-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="de5ce-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de5ce-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de5ce-132"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="de5ce-133">IID</span><span class="sxs-lookup"><span data-stu-id="de5ce-133">IID</span></span><br/>                      | <span data-ttu-id="de5ce-134">IID \_ IMsTscAdvancedSettings se define como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="de5ce-134">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de5ce-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="de5ce-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de5ce-136">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="de5ce-136">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

