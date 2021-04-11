---
description: Cargar un archivo de proyecto
ms.assetid: f8d142bd-e51d-4714-893b-8e3d02506891
title: Cargar un archivo de proyecto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9a710795a29481740bf85390cc7122cc801a22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274707"
---
# <a name="loading-a-project-file"></a><span data-ttu-id="6b747-103">Cargar un archivo de proyecto</span><span class="sxs-lookup"><span data-stu-id="6b747-103">Loading a Project File</span></span>

<span data-ttu-id="6b747-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="6b747-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="6b747-105">Para cargar un archivo de proyecto, necesita dos componentes: el analizador XML y una escala de tiempo vacía.</span><span class="sxs-lookup"><span data-stu-id="6b747-105">To load a project file, you need two components: the XML parser and an empty timeline.</span></span> <span data-ttu-id="6b747-106">El analizador XML Lee un archivo de proyecto XML y crea cada objeto definido en el archivo.</span><span class="sxs-lookup"><span data-stu-id="6b747-106">The XML parser reads an XML project file and creates each object defined in the file.</span></span> <span data-ttu-id="6b747-107">A continuación, inserta los objetos en la escala de tiempo y establece los atributos de la escala de tiempo, como la velocidad de fotogramas predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6b747-107">Then it inserts the objects into the timeline and sets any timeline attributes, such as the default frame rate.</span></span> <span data-ttu-id="6b747-108">En el ejemplo de código siguiente se carga un archivo.</span><span class="sxs-lookup"><span data-stu-id="6b747-108">The following code example loads a file.</span></span>


```C++
HRESULT         hr;
IAMTimeline     *pTL = NULL;
IXml2Dex        *pXML = NULL; 
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
            IID_IAMTimeline, (void**)&pTL);
hr = CoCreateInstance(CLSID_Xml2Dex, NULL, CLSCTX_INPROC_SERVER, 
            IID_IXml2Dex, (void**)&pXML);
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.xtl"), 15);
hr = pXML->ReadXMLFile(pTL, bstrFile); 
SysFreeString(bstrFile);
pXML->Release();
```



<span data-ttu-id="6b747-109">El analizador expone la interfaz [**IXml2Dex**](ixml2dex.md) , que contiene métodos para cargar y guardar archivos de proyecto.</span><span class="sxs-lookup"><span data-stu-id="6b747-109">The parser exposes the [**IXml2Dex**](ixml2dex.md) interface, which contains methods for loading and saving project files.</span></span> <span data-ttu-id="6b747-110">La escala de tiempo expone la interfaz [**IAMTimeline**](iamtimeline.md) , que contiene métodos para manipular la escala de tiempo y crear nuevos objetos Timeline.</span><span class="sxs-lookup"><span data-stu-id="6b747-110">The timeline exposes the [**IAMTimeline**](iamtimeline.md) interface, which contains methods for manipulating the timeline and creating new timeline objects.</span></span> <span data-ttu-id="6b747-111">Llame a la función **CoCreateInstance** para crear cada componente, como se muestra.</span><span class="sxs-lookup"><span data-stu-id="6b747-111">Call the **CoCreateInstance** function to create each component, as shown.</span></span> <span data-ttu-id="6b747-112">Recuerde que, al crear una nueva instancia, está incrementando el recuento de referencias en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="6b747-112">Remember that by creating a new instance, you are incrementing the reference count on the interface.</span></span> <span data-ttu-id="6b747-113">Para evitar pérdidas de memoria, libere siempre una interfaz cuando esté a través de ella.</span><span class="sxs-lookup"><span data-stu-id="6b747-113">To avoid memory leaks, always release an interface when you are through with it.</span></span> <span data-ttu-id="6b747-114">En este ejemplo, el puntero a **IXml2Dex** no es necesario para nada más, por lo que puede liberar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="6b747-114">In this example, the pointer to **IXml2Dex** is not needed for anything more, so you can release the interface.</span></span> <span data-ttu-id="6b747-115">El puntero a **IAMTimeline** sigue siendo necesario para obtener una vista previa de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="6b747-115">The pointer to **IAMTimeline** is still needed for previewing the timeline.</span></span>

<span data-ttu-id="6b747-116">El método [**IXml2Dex:: ReadXMLFile**](ixml2dex-readxmlfile.md) lee el archivo especificado y rellena la escala de tiempo con los objetos definidos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="6b747-116">The [**IXml2Dex::ReadXMLFile**](ixml2dex-readxmlfile.md) method reads the specified file and populates the timeline with the objects defined in the file.</span></span> <span data-ttu-id="6b747-117">El nombre de archivo se especifica mediante un valor **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="6b747-117">The file name is specified using a **BSTR** value.</span></span> <span data-ttu-id="6b747-118">Para acortar el ejemplo, el nombre de archivo en el ejemplo se proporciona como una cadena literal.</span><span class="sxs-lookup"><span data-stu-id="6b747-118">To shorten the example, the file name in the example is given as a literal string.</span></span> <span data-ttu-id="6b747-119">Normalmente, se obtiene de un cuadro de diálogo Abrir archivo o algo similar.</span><span class="sxs-lookup"><span data-stu-id="6b747-119">Normally, you obtain it from an Open File dialog or something similar.</span></span>

<span data-ttu-id="6b747-120">Si el método **ReadXml** se realiza correctamente, devuelve un código de éxito.</span><span class="sxs-lookup"><span data-stu-id="6b747-120">If the **ReadXML** method is successful, it returns a success code.</span></span> <span data-ttu-id="6b747-121">De lo contrario, devuelve un código de error como VFW \_ E \_ no es un formato de \_ archivo válido \_ .</span><span class="sxs-lookup"><span data-stu-id="6b747-121">Otherwise, it returns an error code such as VFW\_E\_INVALID\_FILE\_FORMAT.</span></span> <span data-ttu-id="6b747-122">Compruebe siempre el valor devuelto para controlar correctamente las condiciones de error.</span><span class="sxs-lookup"><span data-stu-id="6b747-122">Always check the return value, in order to handle error conditions gracefully.</span></span> <span data-ttu-id="6b747-123">De nuevo, para mayor brevedad, el código de ejemplo no comprueba si hay errores.</span><span class="sxs-lookup"><span data-stu-id="6b747-123">Again for brevity, the example code does not check for errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b747-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6b747-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b747-125">Cargar y obtener una vista previa de un proyecto</span><span class="sxs-lookup"><span data-stu-id="6b747-125">Loading and Previewing a Project</span></span>](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



