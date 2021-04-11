---
description: Una cadena de regla del descriptor de protección contiene una lista secuencial de uno o más protectores.
ms.assetid: FBFE2143-DC40-40F3-83CE-E6D8841F9C11
title: Descriptores de protección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11814df2af5bd9abee4260f4aadab5bb74c77a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276362"
---
# <a name="protection-descriptors"></a><span data-ttu-id="9f92b-103">Descriptores de protección</span><span class="sxs-lookup"><span data-stu-id="9f92b-103">Protection Descriptors</span></span>

<span data-ttu-id="9f92b-104">Una cadena de regla del descriptor de protección contiene una lista secuencial de uno o más protectores.</span><span class="sxs-lookup"><span data-stu-id="9f92b-104">A protection descriptor rule string contains a sequential list of one or more protectors.</span></span> <span data-ttu-id="9f92b-105">Debe haber al menos un protector.</span><span class="sxs-lookup"><span data-stu-id="9f92b-105">There must be at least one protector.</span></span> <span data-ttu-id="9f92b-106">Si hay más de uno, los protectores deben separarse en la cadena mediante **and** u **or**.</span><span class="sxs-lookup"><span data-stu-id="9f92b-106">If there is more than one, the protectors must be separated in the string by **AND** or **OR**.</span></span> <span data-ttu-id="9f92b-107">Estos valores deben escribirse en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="9f92b-107">These values must be capitalized.</span></span> <span data-ttu-id="9f92b-108">La sintaxis siguiente muestra el formato de cadena de un descriptor de protección.</span><span class="sxs-lookup"><span data-stu-id="9f92b-108">The following syntax shows the string format of a protection descriptor.</span></span>


```C++
Descriptor = [ Protector-or
              *( OR-separator Protector-or ) ]

    Protector-or = Protector-and
              *( AND-separator Protector-and )

    OR-separator = "OR"
    AND-separator = "AND"

    Protector-and = providerName EQUALS providerAttributes

    providerName = descr

    providerAttribute = string | hexstring

      ; The following characters are to be escaped when they appear
      ; in the value to be encoded: ESC, one of <escaped>, leading
      ; SHARP or SPACE, trailing SPACE, and NULL.
      string =   [ ( leadchar / pair ) [ *( stringchar / pair )
         ( trailchar / pair ) ] ]

      leadchar = LUTF1 / UTFMB
      LUTF1 = %x01-1F / %x21 / %x24-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      trailchar  = TUTF1 / UTFMB
      TUTF1 = %x01-1F / %x21 / %x23-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      stringchar = SUTF1 / UTFMB
      SUTF1 = %x01-21 / %x23-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      pair = ESC ( ESC / special / hexpair )
      special = escaped / SPACE / SHARP / EQUALS
      escaped = DQUOTE / PLUS / COMMA / SEMI / LANGLE / RANGLE
      hexstring = SHARP 1*hexpair
      hexpair = HEX HEX

      descr   = leadkeychar *keychar
      leadkeychar = ALPHA
      keychar = ALPHA / DIGIT / HYPHEN
      number  = DIGIT / ( LDIGIT 1*DIGIT )

      ALPHA   = %x41-5A / %x61-7A   ; "A"-"Z" / "a"-"z"
      DIGIT   = %x30 / LDIGIT       ; "0"-"9"
      LDIGIT  = %x31-39             ; "1"-"9"
      HEX     = DIGIT / %x41-46 / %x61-66 ; "0"-"9" / "A"-"F" / "a"-"f"

      NULL    = %x00 ; null (0)
      SPACE   = %x20 ; space (" ")
      DQUOTE  = %x22 ; quote (""")
      SHARP   = %x23 ; octothorpe (or sharp sign) ("#")
      DOLLAR  = %x24 ; dollar sign ("$")
      SQUOTE  = %x27 ; single quote ("'")
      LPAREN  = %x28 ; left paren ("(")
      RPAREN  = %x29 ; right paren (")")
      PLUS    = %x2B ; plus sign ("+")
      COMMA   = %x2C ; comma (",")
      HYPHEN  = %x2D ; hyphen ("-")
      DOT     = %x2E ; period (".")
      SEMI    = %x3B ; semicolon (";")
      LANGLE  = %x3C ; left angle bracket ("<")
      EQUALS  = %x3D ; equals sign ("=")
      RANGLE  = %x3E ; right angle bracket (">")
      ESC     = %x5C ; backslash ("\")
      USCORE  = %x5F ; underscore ("_")
      LCURLY  = %x7B ; left curly brace "{"
      RCURLY  = %x7D ; right curly brace "}"

      ; Any UTF-8 [RFC3629] encoded Unicode [Unicode] character
      UTF8    = UTF1 / UTFMB
      UTFMB   = UTF2 / UTF3 / UTF4
      UTF0    = %x80-BF
      UTF1    = %x00-7F
      UTF2    = %xC2-DF UTF0
      UTF3    = %xE0 %xA0-BF UTF0 / %xE1-EC 2(UTF0) /
                %xED %x80-9F UTF0 / %xEE-EF 2(UTF0)
      UTF4    = %xF0 %x90-BF 2(UTF0) / %xF1-F3 3(UTF0) /
                %xF4 %x80-8F 2(UTF0)

      OCTET   = %x00-FF ; Any octet (8-bit data unit)
```



<span data-ttu-id="9f92b-109">Los descriptores de protección se pueden definir actualmente para los siguientes tipos de autorización:</span><span class="sxs-lookup"><span data-stu-id="9f92b-109">Protection descriptors can currently be defined for the following types of authorization:</span></span>

-   <span data-ttu-id="9f92b-110">Un grupo de un bosque de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9f92b-110">A group in an Active Directory forest.</span></span>
-   <span data-ttu-id="9f92b-111">Un conjunto de credenciales Web.</span><span class="sxs-lookup"><span data-stu-id="9f92b-111">A set of web credentials.</span></span>
-   <span data-ttu-id="9f92b-112">Un certificado en el almacén de certificados del usuario.</span><span class="sxs-lookup"><span data-stu-id="9f92b-112">A certificate in the user's certificate store.</span></span>

<span data-ttu-id="9f92b-113">Entre los ejemplos de cadenas de reglas de descriptor de protección para un grupo de Active Directory se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="9f92b-113">Examples of protection descriptor rule strings for an Active Directory group include the following:</span></span>

-   <span data-ttu-id="9f92b-114">"SID = S-1-5-21-4392301 Y SID = S-1-5-21-3101812"</span><span class="sxs-lookup"><span data-stu-id="9f92b-114">"SID=S-1-5-21-4392301 AND SID=S-1-5-21-3101812"</span></span>
-   <span data-ttu-id="9f92b-115">"SDDL = O:S-1-5-5-0-290724G: SYD: (A;; CCDC;;; S-1-5-5-0-290724) (A;;D C;;; WD) "</span><span class="sxs-lookup"><span data-stu-id="9f92b-115">"SDDL=O:S-1-5-5-0-290724G:SYD:(A;;CCDC;;;S-1-5-5-0-290724)(A;;DC;;;WD)"</span></span>
-   <span data-ttu-id="9f92b-116">"LOCAL = usuario"</span><span class="sxs-lookup"><span data-stu-id="9f92b-116">"LOCAL=user"</span></span>
-   <span data-ttu-id="9f92b-117">"LOCAL = equipo"</span><span class="sxs-lookup"><span data-stu-id="9f92b-117">"LOCAL=machine"</span></span>

<span data-ttu-id="9f92b-118">Entre los ejemplos de cadenas de reglas de descriptor de protección para un conjunto de credenciales Web se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="9f92b-118">Examples of protection descriptor rule strings for a set of web credentials include the following:</span></span>

-   <span data-ttu-id="9f92b-119">"Webcredentials = MyPasswordName"</span><span class="sxs-lookup"><span data-stu-id="9f92b-119">"WEBCREDENTIALS=MyPasswordName"</span></span>
-   <span data-ttu-id="9f92b-120">"Webcredentials = MyPasswordName, myweb. com"</span><span class="sxs-lookup"><span data-stu-id="9f92b-120">"WEBCREDENTIALS=MyPasswordName,myweb.com"</span></span>

<span data-ttu-id="9f92b-121">Entre los ejemplos de cadenas de reglas de descriptor de protección para un certificado se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="9f92b-121">Examples of protection descriptor rule strings for a certificate include the following:</span></span>

-   <span data-ttu-id="9f92b-122">"CERTIFICAte = HashID: \_ hash SHA1 \_ del \_ certificado"</span><span class="sxs-lookup"><span data-stu-id="9f92b-122">"CERTIFICATE=HashID:sha1\_hash\_of\_certificate"</span></span>
-   <span data-ttu-id="9f92b-123">"CERTIFICAte = CertBlob: base64String"</span><span class="sxs-lookup"><span data-stu-id="9f92b-123">"CERTIFICATE=CertBlob:base64String"</span></span>

<span data-ttu-id="9f92b-124">El descriptor de protección que especifique determina automáticamente qué proveedor de protección de claves se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9f92b-124">The protection descriptor you specify automatically determines which key protection provider is used.</span></span> <span data-ttu-id="9f92b-125">Para obtener más información, consulte [proveedores de protección](protection-providers.md).</span><span class="sxs-lookup"><span data-stu-id="9f92b-125">For more information, see [Protection Providers](protection-providers.md).</span></span>

<span data-ttu-id="9f92b-126">Tenga en cuenta que el lado izquierdo del signo igual (=) debe ser **SID**, **SDDL**, **local**, **webcredentials** o **Certificate**.</span><span class="sxs-lookup"><span data-stu-id="9f92b-126">Note that the left side of the equals sign (=) must be **SID**, **SDDL**, **LOCAL**, **WEBCREDENTIALS**, or **CERTIFICATE**.</span></span> <span data-ttu-id="9f92b-127">Estos valores no distinguen entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9f92b-127">These values are not case sensitive.</span></span>

<span data-ttu-id="9f92b-128">Debe especificar una cadena de regla (o un nombre para mostrar asociado a una cadena de regla) cuando llame a la función [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) .</span><span class="sxs-lookup"><span data-stu-id="9f92b-128">You must specify a rule string (or a display name associated with a rule string) when you call the [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) function.</span></span> <span data-ttu-id="9f92b-129">Como alternativa, como las cadenas de reglas del descriptor de protección son bastante complicadas de usar y recordar, puede asociar un nombre para mostrar a la cadena de regla y registrar ambos mediante la función [**NCryptRegisterProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname) .</span><span class="sxs-lookup"><span data-stu-id="9f92b-129">Alternatively, because protection descriptor rule strings are somewhat cumbersome to use and remember, you can associate a display name with the rule string and register both by using the [**NCryptRegisterProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname) function.</span></span> <span data-ttu-id="9f92b-130">Después, puede usar el nombre para mostrar en **NCryptCreateProtectionDescriptor**.</span><span class="sxs-lookup"><span data-stu-id="9f92b-130">Then you can use the display name in **NCryptCreateProtectionDescriptor**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f92b-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9f92b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f92b-132">DPAPI DE CNG</span><span class="sxs-lookup"><span data-stu-id="9f92b-132">CNG DPAPI</span></span>](cng-dpapi.md)
</dt> <dt>

[<span data-ttu-id="9f92b-133">Proveedores de protección</span><span class="sxs-lookup"><span data-stu-id="9f92b-133">Protection Providers</span></span>](protection-providers.md)
</dt> </dl>

 

 



