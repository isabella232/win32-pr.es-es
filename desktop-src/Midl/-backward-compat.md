---
title: Modificador/backward_compat
description: El \_ modificador de compatibilidad/backward indica al compilador de MIDL que desactive algunas características avanzadas al generar código auxiliar de RPC/com.
ms.assetid: eec0ade7-30a0-44e4-92e9-fb03ff657723
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69b558d01b33b99f7d1d9279f729b923ff58df0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676125"
---
# <a name="backward_compat-switch"></a><span data-ttu-id="33b8f-103">/backward ( \_ modificador compatible)</span><span class="sxs-lookup"><span data-stu-id="33b8f-103">/backward\_compat Switch</span></span>

<span data-ttu-id="33b8f-104">El \_ modificador de compatibilidad/backward indica al compilador de MIDL que desactive algunas características avanzadas al generar código auxiliar de RPC/com.</span><span class="sxs-lookup"><span data-stu-id="33b8f-104">The /backward\_compat switch directs the MIDL compiler to turn off some advanced features when generating RPC/COM stubs.</span></span>

``` syntax
midl /backward_compat { maybenull_sizeis | zeroout_alignmentgap | 
     BSTR_byvalue_escaping | string_defaultvalue | signed_wchar_t }
```

## <a name="switch-options"></a><span data-ttu-id="33b8f-105">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="33b8f-105">Switch Options</span></span>

<span data-ttu-id="33b8f-106">*tamaño de maybenull \_*</span><span class="sxs-lookup"><span data-stu-id="33b8f-106">*maybenull\_sizeis*</span></span><dl> <span data-ttu-id="33b8f-107">Aplica el atributo [ \[ deshabilitar \_ \_ comprobación \] de coherencia](disable-consistence-check.md) a una compilación de MIDL completa.</span><span class="sxs-lookup"><span data-stu-id="33b8f-107">Applies the [\[disable\_consistency\_check\]](disable-consistence-check.md) attribute to an entire MIDL compilation.</span></span>  
</dl>

<span data-ttu-id="33b8f-108">*zeroout \_ alignmentgap*</span><span class="sxs-lookup"><span data-stu-id="33b8f-108">*zeroout\_alignmentgap*</span></span><dl> <span data-ttu-id="33b8f-109">Desactiva el llenado de ceros en el búfer de serialización.</span><span class="sxs-lookup"><span data-stu-id="33b8f-109">Turns off zeroing out gaps in the marshaled buffer.</span></span>  
</dl>

<span data-ttu-id="33b8f-110">*Escape de BSTR \_ byvalue \_*</span><span class="sxs-lookup"><span data-stu-id="33b8f-110">*BSTR\_byvalue\_escaping*</span></span><dl> <span data-ttu-id="33b8f-111">Indica al compilador de MIDL que respete las secuencias de escape, como â € ̃ \\ nâ™ o â € ̃ \\ tÂ™ en BSTR.</span><span class="sxs-lookup"><span data-stu-id="33b8f-111">Directs the MIDL compiler to honor escape sequences such as â€˜\\nâ€™ or â€˜\\tâ€™ in BSTRs.</span></span>  
</dl>

<span data-ttu-id="33b8f-112">*cadena \_ DefaultValue*</span><span class="sxs-lookup"><span data-stu-id="33b8f-112">*string\_defaultvalue*</span></span><dl> <span data-ttu-id="33b8f-113">Obliga al compilador de MIDL a convertir las cadenas de los atributos [**\[ DEFAULTVALUE \]**](defaultvalue.md) en Variant. VT \_ I4 Type antes de forzar el valor en el tipo correcto.</span><span class="sxs-lookup"><span data-stu-id="33b8f-113">Forces the MIDL compiler to coerce strings in [**\[defaultvalue\]**](defaultvalue.md) attributes into VARIANT.VT\_I4 type before coercing the value into the correct type.</span></span>  
</dl>

<span data-ttu-id="33b8f-114">*\_WCHAR firmado \_ t*</span><span class="sxs-lookup"><span data-stu-id="33b8f-114">*signed\_wchar\_t*</span></span><dl> <span data-ttu-id="33b8f-115">Indica a MIDL que trate el \_ tipo WCHAR t como firmado para la compatibilidad con Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="33b8f-115">Directs MIDL to treat the wchar\_t type as signed for compatibility with Visual Basic.</span></span>  
</dl>

## <a name="remarks"></a><span data-ttu-id="33b8f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33b8f-116">Remarks</span></span>

-   <span data-ttu-id="33b8f-117">*\_ tamaño de maybenull*: consulte \[ deshabilitar la \_ comprobación de coherencia \_ \] .</span><span class="sxs-lookup"><span data-stu-id="33b8f-117">*maybenull\_sizeis*: See \[disable\_consistency\_check\].</span></span>
-   <span data-ttu-id="33b8f-118">*zeroout \_ alignmentgap*: cuando se compilan pero con â € "Target NT60 o una versión posterior, MIDL creará códigos auxiliares que desconectan cualquier hueco de alineación entre miembros o una estructura en el búfer de conexión.</span><span class="sxs-lookup"><span data-stu-id="33b8f-118">*zeroout\_alignmentgap*: When IDLs are compiled with â€“target NT60 or higher, MIDL will create stubs that zero out any alignment gaps between members or a structure in the wire buffer.</span></span> <span data-ttu-id="33b8f-119">El modificador de línea de comandos */backward \_ compat zeroout \_ ALIGNMENTGAP* dirige a MIDL para deshabilitar esta característica.</span><span class="sxs-lookup"><span data-stu-id="33b8f-119">The command line switch */backward\_compat zeroout\_alignmentgap* directs MIDL to disable this feature.</span></span>

    <span data-ttu-id="33b8f-120">En la estructura de ejemplo siguiente, el búfer de conexión contiene un intervalo de alineación de 7 bytes para alinear el miembro de hipertexto con 8 después del miembro de carácter.</span><span class="sxs-lookup"><span data-stu-id="33b8f-120">In the following example structure, the wire buffer contains a 7 byte alignment gap to align the hyper member to 8 after the char member.</span></span> <span data-ttu-id="33b8f-121">Con "NT60 de destino" o superior, MIDL dejará sin espacio a menos que se use el modificador.</span><span class="sxs-lookup"><span data-stu-id="33b8f-121">With â€“target NT60 or higher, MIDL will zero out that gap unless the switch is used.</span></span>

    <span data-ttu-id="33b8f-122">Archivo IDL:</span><span class="sxs-lookup"><span data-stu-id="33b8f-122">IDL file:</span></span>

    ``` syntax
    typedef struct _structwithgaps{
        char c;
        // 7 byte gap to align the following hyper to 8 
        hyper h;
    } structwithgap;
    ```

    <span data-ttu-id="33b8f-123">Este modificador puede proporcionar una ligera mejora del rendimiento con aumentos potencialmente significativos en el riesgo de divulgación.</span><span class="sxs-lookup"><span data-stu-id="33b8f-123">This switch can provide a slight performance improvement with potentially significant increases in disclosure risk.</span></span>

-   <span data-ttu-id="33b8f-124">*BSTR \_ byvalue \_ Escaping*: de forma predeterminada, el COMpilador de MIDL no procesa secuencias de escape como â € ̃ \\ nÂ €™ o â € ̃ \\ tÂ €™ en constantes de cadena para la automatización OLE al convertir una constante de cadena en tipos VT \_ LPSTR o VT \_ LPWStr.</span><span class="sxs-lookup"><span data-stu-id="33b8f-124">*BSTR\_byvalue\_escaping*: By default, the MIDL compiler does not process escape sequences such as â€˜\\nâ€™ or â€˜\\tâ€™ in string constants for OLE Automation when converting a string constant to types VT\_LPSTR or VT\_LPWSTR.</span></span> <span data-ttu-id="33b8f-125">Con esta opción de cambio de compatibilidad con versiones anteriores, se evalúan las secuencias de escape.</span><span class="sxs-lookup"><span data-stu-id="33b8f-125">With this backward compatibility switch option, the escape sequences are evaluated.</span></span>
-   <span data-ttu-id="33b8f-126">*String \_ DefaultValue*: obliga al compilador de MIDL a convertir las cadenas numéricas de los atributos [**\[ \] DefaultValue**](defaultvalue.md) en Variant. VT \_ I4 Type antes de forzar el valor en el tipo correcto.</span><span class="sxs-lookup"><span data-stu-id="33b8f-126">*string\_defaultvalue*: Forces the MIDL compiler to coerce numeric strings in [**\[defaultvalue\]**](defaultvalue.md) attributes into VARIANT.VT\_I4 type before coercing the value into the correct type.</span></span> <span data-ttu-id="33b8f-127">Esto puede dar lugar a la pérdida de precisión en algunos casos, por lo que no se recomienda esta opción de modificador.</span><span class="sxs-lookup"><span data-stu-id="33b8f-127">This can lead to loss of precision in some cases, so this switch option is not recommended.</span></span>
-   <span data-ttu-id="33b8f-128">*signed \_ WCHAR \_ t*: indica a MIDL que trate el \_ tipo WCHAR t como firmado para la compatibilidad con Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="33b8f-128">*signed\_wchar\_t*: Directs MIDL to treat the wchar\_t type as signed for compatibility with Visual Basic.</span></span>

 

 




