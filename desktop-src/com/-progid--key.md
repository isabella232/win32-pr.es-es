---
title: Clave ProgID
description: Un identificador de programación (ProgID) es una entrada del registro que se puede asociar a un CLSID. Al igual que el CLSID, el ProgID identifica una clase pero con menos precisión porque no se garantiza que sea globalmente único.
ms.assetid: f9ef2934-0815-4a6f-9283-8f748eee083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ef64515d2dda4512af0086970cb2ab61b4830
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078738"
---
# <a name="progid-key"></a><span data-ttu-id="00537-104">Clave ProgID</span><span class="sxs-lookup"><span data-stu-id="00537-104">ProgID Key</span></span>

<span data-ttu-id="00537-105">Un identificador de programación (ProgID) es una entrada del registro que se puede asociar a un CLSID.</span><span class="sxs-lookup"><span data-stu-id="00537-105">A programmatic identifier (ProgID) is a registry entry that can be associated with a CLSID.</span></span> <span data-ttu-id="00537-106">Al igual que el CLSID, el ProgID identifica una clase pero con menos precisión porque no se garantiza que sea globalmente único.</span><span class="sxs-lookup"><span data-stu-id="00537-106">Like the CLSID, the ProgID identifies a class but with less precision because it is not guaranteed to be globally unique.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="00537-107">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="00537-107">Registry Entry</span></span>

<span data-ttu-id="00537-108">**HKEY \_ \_Clases de \\ software \\ de máquina local** \\ *{* ProgID *}*</span><span class="sxs-lookup"><span data-stu-id="00537-108">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes**\\ *{* ProgID *}*</span></span>



| <span data-ttu-id="00537-109">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="00537-109">Registry key</span></span>                            | <span data-ttu-id="00537-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="00537-110">Description</span></span>                                                        |
|-----------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="00537-111">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="00537-111">**CLSID**</span></span>](clsid.md)                  | <span data-ttu-id="00537-112">Asocia un ProgID a un CLSID.</span><span class="sxs-lookup"><span data-stu-id="00537-112">Associates a ProgID with a CLSID.</span></span>                                  |
| [<span data-ttu-id="00537-113">**Insertable**</span><span class="sxs-lookup"><span data-stu-id="00537-113">**Insertable**</span></span>](insertable-progid.md) | <span data-ttu-id="00537-114">Indica que esta clase se va a insertar en contenedores OLE 2.</span><span class="sxs-lookup"><span data-stu-id="00537-114">Indicates that this class is insertable in OLE 2 containers.</span></span>       |
| [<span data-ttu-id="00537-115">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="00537-115">**Protocol**</span></span>](protocol.md)            | <span data-ttu-id="00537-116">Indica que esta clase OLE 2 se va a insertar en contenedores OLE 1.</span><span class="sxs-lookup"><span data-stu-id="00537-116">Indicates that this OLE 2 class is insertable in OLE 1 containers.</span></span> |
| [<span data-ttu-id="00537-117">**Shell**</span><span class="sxs-lookup"><span data-stu-id="00537-117">**Shell**</span></span>](shell.md)                  | <span data-ttu-id="00537-118">Proporciona la impresión del shell de Windows 3,1 y la información **abierta del archivo** .</span><span class="sxs-lookup"><span data-stu-id="00537-118">Provides Windows 3.1 shell printing and **File Open** information.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="00537-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00537-119">Remarks</span></span>

<span data-ttu-id="00537-120">Puede usar un ProgID en situaciones de programación en las que no sea posible usar un CLSID.</span><span class="sxs-lookup"><span data-stu-id="00537-120">You can use a ProgID in programming situations where it is not possible to use a CLSID.</span></span> <span data-ttu-id="00537-121">Los ProgID no deben aparecer en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="00537-121">ProgIDs should not appear in the user interface.</span></span> <span data-ttu-id="00537-122">No se garantiza que los ProgID sean únicos, por lo que solo se pueden usar si los conflictos de nombres son administrables.</span><span class="sxs-lookup"><span data-stu-id="00537-122">ProgIDs are not guaranteed to be unique, so they can be used only where name collisions are manageable.</span></span>

<span data-ttu-id="00537-123">El formato de un ProgID es <*programa*> *. <>* de la *versión* <, separados por puntos y sin espacios, como en> ument. 6.</span><span class="sxs-lookup"><span data-stu-id="00537-123">The format of a ProgID is <*Program*>.<*Component*>.<*Version*>, separated by periods and with no spaces, as in Word.Document.6.</span></span> <span data-ttu-id="00537-124">El ProgID debe cumplir los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="00537-124">The ProgID must comply with the following requirements:</span></span>

-   <span data-ttu-id="00537-125">No debe tener más de 39 caracteres.</span><span class="sxs-lookup"><span data-stu-id="00537-125">Have no more than 39 characters.</span></span>
-   <span data-ttu-id="00537-126">No contenga signos de puntuación (incluidos los guiones bajos) excepto uno o más puntos.</span><span class="sxs-lookup"><span data-stu-id="00537-126">Contain no punctuation (including underscores) except one or more periods.</span></span>
-   <span data-ttu-id="00537-127">No empieza por un dígito.</span><span class="sxs-lookup"><span data-stu-id="00537-127">Not start with a digit.</span></span>
-   <span data-ttu-id="00537-128">Ser diferente del nombre de clase de cualquier aplicación OLE 1, incluida la versión OLE 1 de la misma aplicación, si hay alguna.</span><span class="sxs-lookup"><span data-stu-id="00537-128">Be different from the class name of any OLE 1 application, including the OLE 1 version of the same application, if there is one.</span></span>

<span data-ttu-id="00537-129">Dado que el ProgID no debe aparecer en la interfaz de usuario, puede obtener un nombre que se pueda mostrar llamando a [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype).</span><span class="sxs-lookup"><span data-stu-id="00537-129">Because the ProgID should not appear in the user interface, you can obtain a displayable name by calling [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype).</span></span> <span data-ttu-id="00537-130">Consulte también [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span><span class="sxs-lookup"><span data-stu-id="00537-130">Also, see [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span></span>

<span data-ttu-id="00537-131">La clave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde a la clave **\_ \_ raíz de las clases HKEY** , que se conserva por compatibilidad con versiones anteriores de com.</span><span class="sxs-lookup"><span data-stu-id="00537-131">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00537-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="00537-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00537-133">**IOleObject:: GetUserType**</span><span class="sxs-lookup"><span data-stu-id="00537-133">**IOleObject::GetUserType**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> <dt>

[<span data-ttu-id="00537-134">**OleRegGetUserType**</span><span class="sxs-lookup"><span data-stu-id="00537-134">**OleRegGetUserType**</span></span>](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype)
</dt> </dl>

 

 




