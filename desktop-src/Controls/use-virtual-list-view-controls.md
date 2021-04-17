---
title: Cómo usar controles de List-View virtual
description: En este tema se muestra cómo trabajar con controles de vista de lista virtual.
ms.assetid: DA32D7B3-5FDB-4D73-9A72-0D4EEB2A0C4F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3baf5e37d0d4f6da0cdf596dd8ba3c71e852a99
ms.sourcegitcommit: e584514ced7396dde55e58501c8c8a872229acc4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2021
ms.locfileid: "105660025"
---
# <a name="how-to-use-virtual-list-view-controls"></a><span data-ttu-id="44cd4-103">Cómo usar controles de List-View virtual</span><span class="sxs-lookup"><span data-stu-id="44cd4-103">How to Use Virtual List-View Controls</span></span>

<span data-ttu-id="44cd4-104">En este tema se muestra cómo trabajar con controles de vista de lista virtual.</span><span class="sxs-lookup"><span data-stu-id="44cd4-104">This topic demonstrates how to work with virtual list-view controls.</span></span> <span data-ttu-id="44cd4-105">Los ejemplos de código de C++ que lo acompañan muestran cómo procesar los mensajes de notificación del control de vista de lista virtual, cómo optimizar la memoria caché y cómo recuperar un elemento de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="44cd4-105">The accompanying C++ code examples show how to process virtual list-view control notification messages, how to optimize the cache, and how to retrieve an item from the cache.</span></span>

-   [<span data-ttu-id="44cd4-106">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="44cd4-106">What you need to know</span></span>](#what-you-need-to-know)
-   [<span data-ttu-id="44cd4-107">Procesar códigos de notificación de control de List-View virtual</span><span class="sxs-lookup"><span data-stu-id="44cd4-107">Process Virtual List-View Control Notification Codes</span></span>](#process-virtual-list-view-control-notification-codes)
-   [<span data-ttu-id="44cd4-108">Optimizar la memoria caché</span><span class="sxs-lookup"><span data-stu-id="44cd4-108">Optimize the Cache</span></span>](#optimize-the-cache)
-   [<span data-ttu-id="44cd4-109">Recuperar un elemento de la memoria caché</span><span class="sxs-lookup"><span data-stu-id="44cd4-109">Retrieve an Item From the Cache</span></span>](#retrieve-an-item-from-the-cache)
-   [<span data-ttu-id="44cd4-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="44cd4-110">Related topics</span></span>](#related-topics)

> [!Note]  
> <span data-ttu-id="44cd4-111">En el código de ejemplo de esta sección se supone que la memoria caché es una matriz asignada dinámicamente de estructuras definidas por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="44cd4-111">The example code in this section assumes that the cache is a dynamically allocated array of application-defined structures.</span></span> <span data-ttu-id="44cd4-112">La estructura se define en el siguiente ejemplo de código de C++.</span><span class="sxs-lookup"><span data-stu-id="44cd4-112">The structure is defined in the following C++ code example.</span></span>

 


```C++
struct RndItem
{
    int   iIcon;                 // Bitmap assigned to this item.
    UINT  state;                 // Item state value.
    TCHAR Title[BUFFER_SIZE];    // BUFFER_SIZE is a user-defined macro value.
    TCHAR SubText1[BUFFER_SIZE]; // Text for the label of the first sub-item.
    TCHAR SubText2[BUFFER_SIZE]; // Text for the label of the second item.
};

```



## <a name="what-you-need-to-know"></a><span data-ttu-id="44cd4-113">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="44cd4-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="44cd4-114">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="44cd4-114">Technologies</span></span>

-   [<span data-ttu-id="44cd4-115">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="44cd4-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="44cd4-116">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="44cd4-116">Prerequisites</span></span>

-   <span data-ttu-id="44cd4-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="44cd4-117">C/C++</span></span>
-   <span data-ttu-id="44cd4-118">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="44cd4-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="44cd4-119">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="44cd4-119">Instructions</span></span>

### <a name="process-virtual-list-view-control-notification-codes"></a><span data-ttu-id="44cd4-120">Procesar códigos de notificación de control de List-View virtual</span><span class="sxs-lookup"><span data-stu-id="44cd4-120">Process Virtual List-View Control Notification Codes</span></span>

<span data-ttu-id="44cd4-121">Además de los códigos de notificación enviados por otros controles de vista de lista, los controles de vista de lista virtual también pueden enviar los códigos de notificación [LVN \_ ODCACHEHINT](lvn-odcachehint.md) y [**LVN \_ ODFINDITEM**](lvn-odfinditem.md) .</span><span class="sxs-lookup"><span data-stu-id="44cd4-121">In addition to the notification codes sent by other list-view controls, virtual list-view controls can also send the [LVN\_ODCACHEHINT](lvn-odcachehint.md) and [**LVN\_ODFINDITEM**](lvn-odfinditem.md) notification codes.</span></span>

<span data-ttu-id="44cd4-122">Esta función definida por la aplicación controla los mensajes de notificación que se envían normalmente desde un control de vista de lista virtual.</span><span class="sxs-lookup"><span data-stu-id="44cd4-122">This application-defined function handles notification messages that are commonly sent from a virtual list-view control.</span></span>


```C++
LRESULT OnNotify(HWND hwnd, NMHDR* pnmhdr)
{
    HRESULT hr;
    LRESULT lrt = FALSE;

    switch (pnmhdr->code)
    {
    case LVN_GETDISPINFO:
        {
            RndItem rndItem;
            NMLVDISPINFO* plvdi = (NMLVDISPINFO*) pnmhdr;

            if (-1 == plvdi->item.iItem)
            {
                OutputDebugString(TEXT("LVOWNER: Request for -1 item?\n"));
                DebugBreak();
            }

            // Retrieve information for item at index iItem.
            RetrieveItem( &rndItem, plvdi->item.iItem );

            if(plvdi->item.mask & LVIF_STATE)
            {
                // Fill in the state information.
                plvdi->item.state |= rndItem.state;
            }

            if(plvdi->item.mask & LVIF_IMAGE)
            {
                // Fill in the image information.
                plvdi->item.iImage = rndItem.iIcon;
            }

            if(plvdi->item.mask & LVIF_TEXT)
            {
                // Fill in the text information.
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // Copy the main item text.
                    hr = StringCchCopy(plvdi->item.pszText, MAX_COUNT, rndItem.Title);

                    if(FAILED(hr))
                    { 
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter                                
                        // more characters than specified by MAX_COUNT or  
                        // the text will be truncated.
                    }
                    break;

                case 1:
                    // Copy SubItem1 text.
                    hr = StringCchCopy( plvdi->item.pszText, MAX_COUNT, rndItem.SubText1);

                    if(FAILED(hr))
                    {
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter               
                        // more characters than specified by MAX_COUNT or   
                        // the text will be truncated..
                    }
                    break;

                case 2:
                    // Copy SubItem2 text.
                    hr = StringCchCopy(plvdi->item.pszText, MAX_COUNT, rndItem.SubText2);

                    if(FAILED(hr))
                    {
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter                    
                        // more characters than specified by MAX_COUNT or  
                        // the text will be truncated..
                    }
                    break;

                default:
                    break;

                }

            }

            lrt = FALSE;
            break;
        }

    case LVN_ODCACHEHINT:
        {
            NMLVCACHEHINT* pcachehint = (NMLVCACHEHINT*) pnmhdr;

            // Load the cache with the recommended range.
            PrepCache( pcachehint->iFrom, pcachehint->iTo );
            break;
        }

    case LVN_ODFINDITEM:
        {
            LPNMLVFINDITEM pnmfi = NULL;
            
            pnmfi = (LPNMLVFINDITEM)pnmhdr;

            // Call a user-defined function that finds the index according to
            // LVFINDINFO (which is embedded in the LPNMLVFINDITEM structure).
            // If nothing is found, then set the return value to -1.

            break;
        }

    default:
        break;

    }       // End Switch block.

    return(lrt);
}
```



### <a name="optimize-the-cache"></a><span data-ttu-id="44cd4-123">Optimizar la memoria caché</span><span class="sxs-lookup"><span data-stu-id="44cd4-123">Optimize the Cache</span></span>

<span data-ttu-id="44cd4-124">Un control de vista de lista virtual envía un mensaje de notificación de [LVN \_ ODCACHEHINT](lvn-odcachehint.md) cuando cambia el contenido de su área de presentación.</span><span class="sxs-lookup"><span data-stu-id="44cd4-124">A virtual list-view control sends a [LVN\_ODCACHEHINT](lvn-odcachehint.md) notification message when the contents of its display area have changed.</span></span> <span data-ttu-id="44cd4-125">El mensaje contiene información sobre el intervalo de elementos que se va a almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="44cd4-125">The message contains information about the range of items to be cached.</span></span> <span data-ttu-id="44cd4-126">Tras recibir el mensaje de notificación, la aplicación debe estar preparada para cargar la memoria caché con información del elemento para el intervalo solicitado, de modo que la información estará disponible fácilmente cuando se envíe un mensaje de notificación [ \_ GETDISPINFO de LVN](lvn-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="44cd4-126">Upon receiving the notification message, your application must be prepared to load the cache with item information for the requested range so that the information will be readily available when an [LVN\_GETDISPINFO](lvn-getdispinfo.md) notification message is sent.</span></span>

<span data-ttu-id="44cd4-127">En el siguiente ejemplo de código de C++, la función definida por la aplicación acepta el intervalo de elementos de la memoria caché que envía un control de vista de lista virtual.</span><span class="sxs-lookup"><span data-stu-id="44cd4-127">In the following C++ code example, the application-defined function accepts the range of items for the cache that is sent by a virtual list-view control.</span></span> <span data-ttu-id="44cd4-128">Realiza una comprobación para determinar que el intervalo de elementos solicitado no se ha almacenado en la memoria caché y, a continuación, asigna la memoria global necesaria y rellena la memoria caché si es necesario.</span><span class="sxs-lookup"><span data-stu-id="44cd4-128">It performs a verification to determine that the requested range of items is not already cached, and then it allocates the required global memory and fills the cache if necessary.</span></span>


```C++
void PrepCache(int iFrom, int iTo)
{
    /*  Global Variables

     *  g_priCache[ ]: the main cache.
     *  g_iCache:      the index of the first item in the main cache.
     *  g_cCache:      the count of items in the main cache.
     *
     *  g_priEndCache[ ]: the cache of items at the end of the list.
     *  g_iEndCache:      the index of the first item in the end cache.
     *  g_cEndCache:      the count of items in the end cache.
     */
     
    // Local Variables
    int i;
    BOOL fOLFrom = FALSE;
    BOOL   fOLTo = FALSE;

    // Check to see if this is the end cache.
    if ((iTo == g_cCache - 1) && ((iTo - iFrom) < 30))  // 30 entries wide.
    {
        // Check to see if this is a portion of the current end cache.
        if ((g_cCache) && (iFrom >= g_iEndCache) && (iFrom < g_iEndCache+g_cEndCache))
            return;
            // If it is a part of current end cache, no loading is necessary.

        // This is a new end cache. Free the old memory.
        if ( g_priEndCache )
            GlobalFree( g_priEndCache );
            
        // Set the index and count values for the new end cache,
        // and then retrieve the memory.
        g_iEndCache   = iFrom;
        g_cEndCache   = (iTo - iFrom + 1);
        g_priEndCache = (RndItem *)GlobalAlloc(GPTR, sizeof(RndItem) * g_cEndCache);

        if (! g_priEndCache)
        {
            // TODO: Out of memory. Perform error handling.
        }

        // Loop to fill the cache with the recommended items.
        for (i=0; i<g_cEndCache; i++)
        {
            // TODO: Call a function that accesses item information and
            // fills a cache element.
        }
    }

    else
    {   
        // It is not a member of the current end cache.
        // Try the primary cache instead.

        // Check to see if iFrom is within the primary cache.
        if ((g_cCache) && (iFrom >= g_iCache) && (iFrom < g_iCache+g_cCache))
            fOLFrom = TRUE;

        // Check to see if iTo is within the primary cache.
        if ((g_cCache) && (iTo >= g_iCache) && (iTo <= g_iCache+g_cCache))
            fOLTo = TRUE;

        // do nothing if both iFrom and iTo are within the current cache.

        if (fOLFrom && fOLTo)
            return;

        // Enlarge the cache size rather than make it specific to this hint.
        if (fOLFrom)
            iFrom = g_iCache;

        else if (fOLTo)
            iTo = g_iCache + g_cCache;

        // A new primary cache is needed. Free the old primary cache.
        if ( g_priCache )
            GlobalFree( g_priCache );

        // Set the index and count values for the new primary cache,
        // and then retrieve the memory.
        g_iCache   = iFrom;
        g_cCache   = (iTo - iFrom + 1);
        g_priCache = (RndItem *)GlobalAlloc( GPTR, sizeof( RndItem ) * g_cCache );

        if (!g_priCache)
        {
            // TODO: Out of memory. Do error handling.
        }

        // Loop to fill the cache with the recommended items.
        for (i=0; i<g_cCache; i++)
        {
            // TODO: Call a function that accesses item information
            // and fills a cache element.
        }
    }
}
```



### <a name="retrieve-an-item-from-the-cache"></a><span data-ttu-id="44cd4-129">Recuperar un elemento de la memoria caché</span><span class="sxs-lookup"><span data-stu-id="44cd4-129">Retrieve an Item From the Cache</span></span>

<span data-ttu-id="44cd4-130">Esta función de ejemplo acepta dos parámetros, la dirección de la estructura definida por la aplicación y un valor entero que representa el índice del elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="44cd4-130">This example function accepts two parameters, the address of the application-defined structure and an integer value representing the index of the item in the list.</span></span> <span data-ttu-id="44cd4-131">Comprueba el valor de índice para detectar si el elemento deseado está almacenado en caché.</span><span class="sxs-lookup"><span data-stu-id="44cd4-131">It checks the index value to discover if the desired item is cached.</span></span> <span data-ttu-id="44cd4-132">Si es así, el puntero que se pasó a la función se establece en una ubicación en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="44cd4-132">If it is, the pointer that was passed to the function is set to a location in the cache.</span></span> <span data-ttu-id="44cd4-133">Si el elemento no está en la memoria caché principal o final, la información del elemento debe encontrarse manualmente.</span><span class="sxs-lookup"><span data-stu-id="44cd4-133">If the item is not in the main or end cache, the item information must be located manually.</span></span>


```C++
void RetrieveItem( RndItem * prndItem, int index )
{
    // Global Variables

    // g_priCache[ ]: the main cache.
    // g_iCache:      the index of the first item in the main cache.
    // c_cCache:      the count of items in the main cache.
    //
    // g_priEndCache[ ]:  the cache of items at the end of the list.
    // g_iEndCache:       the index of the first item in the end cache.
    // g_cEndCache:       the count of items in the end cache.
    //

    // Check to see if the item is in the main cache.
    if ((index >= g_iCache) && (index < g_iCache + g_cCache))
        *prndItem = g_priCache[index-g_iCache];

    // If it is not in the main cache, then check to see if
    // the item is in the end area cache.
    else if ((index >= g_iEndCache) && (index < g_iEndCache + g_cEndCache))
        *prndItem = g_priEndCache[index-g_iEndCache];

    else
    {
        // The item is not in either cache.
        // Therefore, retrieve the item information manually.
    }
}
```



## <a name="remarks"></a><span data-ttu-id="44cd4-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44cd4-134">Remarks</span></span>

<span data-ttu-id="44cd4-135">Para obtener una lista de los mensajes de ventana procesados por un control de vista de lista, vea [Default List-View Message Processing](listview-message-processing.md).</span><span class="sxs-lookup"><span data-stu-id="44cd4-135">For a list of the window messages processed by a list-view control, see [Default List-View Message Processing](listview-message-processing.md).</span></span>

## <a name="complete-example"></a><span data-ttu-id="44cd4-136">Ejemplo completo</span><span class="sxs-lookup"><span data-stu-id="44cd4-136">Complete example</span></span>

## <a name="related-topics"></a><span data-ttu-id="44cd4-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="44cd4-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44cd4-138">Referencia de control de vista de lista</span><span class="sxs-lookup"><span data-stu-id="44cd4-138">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="44cd4-139">Acerca de los controles List-View</span><span class="sxs-lookup"><span data-stu-id="44cd4-139">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="44cd4-140">Usar controles List-View</span><span class="sxs-lookup"><span data-stu-id="44cd4-140">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




