---
title: palabra clave Union (RPC)
description: Las uniones requieren palabras clave MIDL especiales para admitir su uso con la llamada a procedimiento remoto (RPC).
ms.assetid: e7c8296c-893d-4df7-913a-f969733e1917
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c562815d78ab931bd4d6590b5465647e72f4bf6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359009"
---
# <a name="union-keyword-rpc"></a><span data-ttu-id="98af7-103">palabra clave Union (RPC)</span><span class="sxs-lookup"><span data-stu-id="98af7-103">union keyword (RPC)</span></span>

<span data-ttu-id="98af7-104">Algunas características del lenguaje C, como uniones, requieren palabras clave MIDL especiales para admitir su uso en llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="98af7-104">Some features of the C language, such as unions, require special MIDL keywords to support their use in remote procedure calls.</span></span> <span data-ttu-id="98af7-105">Una Unión en el lenguaje C es una variable que contiene objetos de diferentes tipos y tamaños.</span><span class="sxs-lookup"><span data-stu-id="98af7-105">A union in the C language is a variable that holds objects of different types and sizes.</span></span> <span data-ttu-id="98af7-106">Normalmente, el desarrollador crea una variable para realizar un seguimiento de los tipos almacenados en la Unión.</span><span class="sxs-lookup"><span data-stu-id="98af7-106">The developer usually creates a variable to keep track of the types stored in the union.</span></span> <span data-ttu-id="98af7-107">Para que funcione correctamente en un entorno distribuido, la variable que indica el tipo de Unión, o *discriminante*, también debe estar disponible en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="98af7-107">To operate correctly in a distributed environment, the variable that indicates the type of the union, or the *discriminant*, must also be available to the remote computer.</span></span> <span data-ttu-id="98af7-108">MIDL proporciona el \[ [**\_ tipo de modificador**](/windows/desktop/Midl/switch-type) \] y el \[ [**modificador \_ son**](/windows/desktop/Midl/switch-is) \] palabras clave para identificar el tipo y el nombre de discriminante.</span><span class="sxs-lookup"><span data-stu-id="98af7-108">MIDL provides the \[[**switch\_type**](/windows/desktop/Midl/switch-type)\] and \[[**switch\_is**](/windows/desktop/Midl/switch-is)\] keywords to identify the discriminant type and name.</span></span>

<span data-ttu-id="98af7-109">MIDL requiere que el discriminante se transmita con la Unión de una de estas dos maneras:</span><span class="sxs-lookup"><span data-stu-id="98af7-109">MIDL requires that the discriminant be transmitted with the union in one of two ways:</span></span>

-   <span data-ttu-id="98af7-110">La Unión y discriminante se deben proporcionar como parámetros.</span><span class="sxs-lookup"><span data-stu-id="98af7-110">The union and the discriminant must be provided as parameters.</span></span>
-   <span data-ttu-id="98af7-111">La Unión y discriminante se deben empaquetar en una estructura.</span><span class="sxs-lookup"><span data-stu-id="98af7-111">The union and the discriminant must be packaged in a structure.</span></span>

<span data-ttu-id="98af7-112">MIDL proporciona dos tipos fundamentales de uniones discriminadas: [**\_ Unión no encapsulada**](/windows/desktop/Midl/nonencapsulated-unions) y [**\_ Unión encapsulada**](/windows/desktop/Midl/encapsulated-unions).</span><span class="sxs-lookup"><span data-stu-id="98af7-112">Two fundamental types of discriminated unions are provided by MIDL: [**nonencapsulated\_union**](/windows/desktop/Midl/nonencapsulated-unions) and [**encapsulated\_union**](/windows/desktop/Midl/encapsulated-unions).</span></span> <span data-ttu-id="98af7-113">El discriminante de una Unión no encapsulada es otro parámetro si la Unión es un parámetro.</span><span class="sxs-lookup"><span data-stu-id="98af7-113">The discriminant of a nonencapsulated union is another parameter if the union is a parameter.</span></span> <span data-ttu-id="98af7-114">Es otro campo si la Unión es un campo de una estructura.</span><span class="sxs-lookup"><span data-stu-id="98af7-114">It is another field if the union is a field of a structure.</span></span> <span data-ttu-id="98af7-115">La definición de una Unión encapsulada se convierte en una definición de estructura cuyo primer campo es el discriminante y cuyo segundo y último campos son la Unión.</span><span class="sxs-lookup"><span data-stu-id="98af7-115">The definition of an encapsulated union is turned into a structure definition whose first field is the discriminant and whose second and last fields are the union.</span></span> <span data-ttu-id="98af7-116">En el ejemplo siguiente se muestra cómo proporcionar la Unión y discriminante como parámetros:</span><span class="sxs-lookup"><span data-stu-id="98af7-116">The following example demonstrates how to provide the union and discriminant as parameters:</span></span>

``` syntax
typedef [switch_type(short)] union 
{
    [case(0)]    short     sVal;
    [case(1)]    float     fVal;
    [case(2)]    char      chVal;
    [default]    ;
} DISCRIM_UNION_PARAM_TYPE;
 
short UnionParamProc(
    [in, switch_is(sUtype)] DISCRIM_UNION_PARAM_TYPE Union,
    [in] short sUtype);
```

<span data-ttu-id="98af7-117">En el ejemplo anterior, la Unión puede contener un valor único: **Short**, **float** o **Char**.</span><span class="sxs-lookup"><span data-stu-id="98af7-117">The union in the preceding example can contain a single value: either **short**, **float**, or **char**.</span></span> <span data-ttu-id="98af7-118">La definición de tipo para la Unión incluye el atributo de **\_ tipo de modificador** MIDL que especifica el tipo de discriminante.</span><span class="sxs-lookup"><span data-stu-id="98af7-118">The type definition for the union includes the MIDL **switch\_type** attribute that specifies the type of the discriminant.</span></span> <span data-ttu-id="98af7-119">Aquí, \[ \_ el tipo de conmutador (short) \] especifica que discriminante es de tipo **Short**.</span><span class="sxs-lookup"><span data-stu-id="98af7-119">Here, \[switch\_type(short)\] specifies that the discriminant is of type **short**.</span></span> <span data-ttu-id="98af7-120">El modificador debe ser un tipo entero.</span><span class="sxs-lookup"><span data-stu-id="98af7-120">The switch must be an integer type.</span></span>

<span data-ttu-id="98af7-121">Si la Unión es un miembro de una estructura, el discriminante debe ser un miembro de la misma estructura.</span><span class="sxs-lookup"><span data-stu-id="98af7-121">If the union is a member of a structure, then the discriminant must be a member of the same structure.</span></span> <span data-ttu-id="98af7-122">Si la Unión es un parámetro, el discriminante debe ser otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="98af7-122">If the union is a parameter, then the discriminant must be another parameter.</span></span> <span data-ttu-id="98af7-123">El prototipo de la función **UnionParamProc** en el ejemplo anterior muestra discriminante *sUtype* como el último parámetro de la llamada.</span><span class="sxs-lookup"><span data-stu-id="98af7-123">The prototype for the function **UnionParamProc** in the preceding example shows the discriminant *sUtype* as the last parameter of the call.</span></span> <span data-ttu-id="98af7-124">(Discriminante puede aparecer en cualquier posición de la llamada). El tipo del parámetro especificado en el **\[ modificador \_ es \]** el atributo debe coincidir con el tipo especificado en el atributo de **\[ \_ \] tipo de conmutador** .</span><span class="sxs-lookup"><span data-stu-id="98af7-124">(The discriminant can appear in any position in the call.) The type of the parameter specified in the **\[switch\_is\]** attribute must match the type specified in the **\[switch\_type\]** attribute.</span></span>

<span data-ttu-id="98af7-125">En el ejemplo siguiente se muestra el uso de una única estructura que empaqueta discriminante con la Unión:</span><span class="sxs-lookup"><span data-stu-id="98af7-125">The following example demonstrates the use of a single structure that packages the discriminant with the union:</span></span>

``` syntax
typedef struct 
{
    short utype;  /* discriminant can precede or follow union */
    [switch_is(utype)] union 
    {
       [case(0)]   short     sVal;
       [case(1)]   float     fVal;
       [case(2)]   char      chVal;
       [default]   ;
    } u;
} DISCRIM_UNION_STRUCT_TYPE;
 
short UnionStructProc(
    [in] DISCRIM_UNION_STRUCT_TYPE u1);
```

<span data-ttu-id="98af7-126">El compilador de Microsoft RPC MIDL permite declaraciones Union fuera de las construcciones [**typedef**](/windows/desktop/Midl/typedef) .</span><span class="sxs-lookup"><span data-stu-id="98af7-126">The Microsoft RPC MIDL compiler allows union declarations outside of [**typedef**](/windows/desktop/Midl/typedef) constructs.</span></span> <span data-ttu-id="98af7-127">Esta característica es una extensión de DCE IDL.</span><span class="sxs-lookup"><span data-stu-id="98af7-127">This feature is an extension to DCE IDL.</span></span> <span data-ttu-id="98af7-128">Para obtener más información, consulte [**Union**](/windows/desktop/Midl/union).</span><span class="sxs-lookup"><span data-stu-id="98af7-128">For more information, see [**union**](/windows/desktop/Midl/union).</span></span>

 

 