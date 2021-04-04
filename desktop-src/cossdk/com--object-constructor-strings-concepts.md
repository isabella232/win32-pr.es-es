---
description: Las cadenas del constructor de objetos COM+ son cadenas de inicialización que se especifican administrativamente para un componente.
ms.assetid: b4915dae-c97c-4d36-95ee-bb10dcb40845
title: Conceptos de las cadenas del constructor de objetos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32bffd35ad230efe1f22b52da10e1b4910d71da
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998200"
---
# <a name="com-object-constructor-strings-concepts"></a><span data-ttu-id="aee53-103">Conceptos de las cadenas del constructor de objetos COM+</span><span class="sxs-lookup"><span data-stu-id="aee53-103">COM+ Object Constructor Strings Concepts</span></span>

<span data-ttu-id="aee53-104">Las cadenas del constructor de objetos COM+ son cadenas de inicialización que se especifican administrativamente para un componente.</span><span class="sxs-lookup"><span data-stu-id="aee53-104">COM+ object constructor strings are initialization strings that are administratively specified for a component.</span></span> <span data-ttu-id="aee53-105">Puede usar cadenas de constructor de objeto para escribir un único componente con un grado de generalidad que permita que se personalice más adelante para una tarea determinada. es decir, puede realizar la construcción de objetos parametrizados.</span><span class="sxs-lookup"><span data-stu-id="aee53-105">You can use object constructor strings to write a single component with a degree of generality that allows it to be later customized for a particular task; that is, you can perform parameterized object construction.</span></span>

<span data-ttu-id="aee53-106">Por ejemplo, puede usar esta característica para escribir un componente que contenga una conexión ODBC genérica y, posteriormente, especificar un DSN exacto para el componente de forma administrativa.</span><span class="sxs-lookup"><span data-stu-id="aee53-106">For example, you might use this feature to write a component that holds a generic ODBC connection and later specify an exact DSN for the component administratively.</span></span> <span data-ttu-id="aee53-107">Si cambia la configuración del sistema, puede cambiar la cadena del constructor en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="aee53-107">If the system configuration changes, you can change the constructor string accordingly.</span></span>

> [!Note]  
> <span data-ttu-id="aee53-108">Las cadenas del constructor de objetos no deben usarse para almacenar información confidencial de seguridad.</span><span class="sxs-lookup"><span data-stu-id="aee53-108">Object constructor strings should not be used to store security-sensitive information.</span></span>

 

<span data-ttu-id="aee53-109">Puede utilizar cadenas del constructor de objetos junto con la [agrupación de objetos](com--object-pooling.md) para lograr un mayor grado de granularidad en la forma en que agrupa y reutiliza los recursos.</span><span class="sxs-lookup"><span data-stu-id="aee53-109">You can use object constructor strings in conjunction with [object pooling](com--object-pooling.md) to achieve a greater degree of granularity in how you pool and reuse resources.</span></span> <span data-ttu-id="aee53-110">Por ejemplo, podría crear varios componentes distintos, idénticos a excepción de las cadenas de constructor y los CLSID, para mantener distintos grupos de objetos que contengan conexiones que puedan usar los distintos grupos de clientes.</span><span class="sxs-lookup"><span data-stu-id="aee53-110">For example, you might create several distinct components, identical except for constructor strings and CLSIDs, to maintain distinct pools of objects holding connections usable by distinct groups of clients.</span></span> <span data-ttu-id="aee53-111">Esto sería útil si las conexiones se abren de forma que las enlaza a roles de seguridad determinados, como cuando las conexiones se abren con cierta autenticación específica en la base de datos, lo que las representa en el caso general.</span><span class="sxs-lookup"><span data-stu-id="aee53-111">This would be useful if connections are opened in a manner that binds them to particular security roles—such as when the connections are opened with some specific authentication at the database—rendering them non-reusable in the general case.</span></span>

<span data-ttu-id="aee53-112">Para ello, puede escribir un único componente genérico que se base en cadenas de constructor de objetos, mediante [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct), y volver a compilarlo para generar varios componentes personalizables con un CLSID distinto.</span><span class="sxs-lookup"><span data-stu-id="aee53-112">To do this, you can write a single generic component that relies on object constructor strings, using [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct), and recompile it to produce several customizable components each with a distinct CLSID.</span></span> <span data-ttu-id="aee53-113">Después, puede adaptar administrativamente cada componente para abrir una conexión adecuada con una cadena de constructor, configurarlos para que se agrupen y se mantendrán en grupos distintos por CLSID.</span><span class="sxs-lookup"><span data-stu-id="aee53-113">You can then administratively tailor each component to open an appropriate connection with a constructor string, configure them to be pooled, and they will be maintained in distinct pools per CLSID.</span></span>

<span data-ttu-id="aee53-114">Puede especificar una cadena de constructor cuando un componente se ha escrito específicamente para reconocer la cadena que especifique.</span><span class="sxs-lookup"><span data-stu-id="aee53-114">You can specify a constructor string when a component has been written specifically to recognize the string that you enter.</span></span> <span data-ttu-id="aee53-115">Los componentes pueden tener acceso mediante programación a estas cadenas mediante [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct).</span><span class="sxs-lookup"><span data-stu-id="aee53-115">Components can access these strings programmatically by using [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct).</span></span>

<span data-ttu-id="aee53-116">Las cadenas de constructor se pasan en el momento de creación del objeto solo cuando la construcción del objeto está habilitada de forma administrativa.</span><span class="sxs-lookup"><span data-stu-id="aee53-116">Constructor strings are passed in at object creation time only when object construction is administratively enabled.</span></span> <span data-ttu-id="aee53-117">COM+ llama al método [**IObjectConstruct:: Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) que implementa.</span><span class="sxs-lookup"><span data-stu-id="aee53-117">COM+ calls the [**IObjectConstruct::Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) method that it implements.</span></span> <span data-ttu-id="aee53-118">Dentro de ese método, puede tener acceso a la cadena del constructor mediante [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring).</span><span class="sxs-lookup"><span data-stu-id="aee53-118">Within that method, you can access the constructor string by using [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring).</span></span> <span data-ttu-id="aee53-119">Las cadenas vacías pueden ser entradas válidas.</span><span class="sxs-lookup"><span data-stu-id="aee53-119">Empty strings can be valid entries.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aee53-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aee53-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aee53-121">Agrupación de objetos COM+</span><span class="sxs-lookup"><span data-stu-id="aee53-121">COM+ Object Pooling</span></span>](com--object-pooling.md)
</dt> <dt>

[<span data-ttu-id="aee53-122">Especificar una cadena de constructor de objeto para un componente</span><span class="sxs-lookup"><span data-stu-id="aee53-122">Specifying an Object Constructor String for a Component</span></span>](specifying-an-object-constructor-string-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="aee53-123">Usar una cadena de constructor de objeto para construir un componente</span><span class="sxs-lookup"><span data-stu-id="aee53-123">Using an Object Constructor String to Construct a Component</span></span>](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



