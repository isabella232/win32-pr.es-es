---
title: Programar ADSI con Java/COM
description: Con la máquina virtual de Microsoft para Java (máquina virtual de Microsoft) y el compilador de Microsoft Java, tiene acceso a todas las características de ADSI expuestas a través de los componentes COM ADSI, desde una aplicación Java/COM.
ms.assetid: eda516b6-0f89-464f-a9d2-9bb4ca70fda5
ms.tgt_platform: multiple
keywords:
- Programar ADSI con Java/COM AD
- ADSI ADSI, usar, programación con Java/COM para
- ADSI ADSI, código de ejemplo Java
- ADSI ADSI, código de ejemplo Java, enlazar a un objeto ADSI e invocar métodos en ese objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6899804208f9899823f266bc941bcf3c2dec372
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903035"
---
# <a name="programming-adsi-with-javacom"></a><span data-ttu-id="cf90a-107">Programar ADSI con Java/COM</span><span class="sxs-lookup"><span data-stu-id="cf90a-107">Programming ADSI with Java/COM</span></span>

<span data-ttu-id="cf90a-108">Con la máquina virtual de Microsoft para Java (máquina virtual de Microsoft) y el compilador de Microsoft Java, tiene acceso a todas las características de ADSI expuestas a través de los componentes COM ADSI, desde una aplicación Java/COM.</span><span class="sxs-lookup"><span data-stu-id="cf90a-108">Using the Microsoft virtual machine for Java (Microsoft VM) and Microsoft Java Compiler, you have access to all the ADSI features exposed through any ADSI COM components, from a Java/COM application.</span></span> <span data-ttu-id="cf90a-109">En el siguiente ejemplo de código de Java se muestran los elementos necesarios para enlazar a un objeto ADSI e invocar métodos en ese objeto.</span><span class="sxs-lookup"><span data-stu-id="cf90a-109">The following Java code example shows the elements necessary to bind to an ADSI object and invoke methods on that object.</span></span> <span data-ttu-id="cf90a-110">Los métodos de objeto y las funciones de la API ADSI necesarios se exponen a través de Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="cf90a-110">The required ADSI API functions and object methods are exposed through Activeds.dll.</span></span>


```C++
import activeds.*;       // ADSI COM Wrapper classes
import com.ms.com.*;     // to use _Guid data type in COM.

public Class SimpleADSI 
{
    IADs obj;
    String path = "WinNT://domain/machine,computer";
    _Guid riid = IADs.iid;
    public static void main(String args[]) 
    {
        try 
        {
            obj = (IADs)ADsGetObject(path, riid);
            System.out.println( "Object name:  " + obj.getName() );
            System.out.println( "      class:  " + obj.getSchema() );
            System.out.println( "    ADsPath:  " + obj.getADsPath() );
            System.out.println( "     parent:  " + obj.getParent() );
        }
        catch (Exception e) 
        {
            System.out.println( "SimpleADSI Error: " + e.toString() );
        }
    }

    /** @dll.import("activeds", ole) */
    private static native IUnknown ADsGetObject(String path, _Guid riid);
}
```



<span data-ttu-id="cf90a-111">El argumento de la primera instrucción **Import** hace referencia a las clases contenedoras de Java empaquetadas en Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="cf90a-111">The argument in the first **import** statement refers to Java Wrapper classes packaged in Activeds.dll.</span></span> <span data-ttu-id="cf90a-112">Use Visual J++ para crear las clases contenedoras e incluirlas en el proyecto siguiendo el procedimiento que se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="cf90a-112">Use Visual J++ to create the wrapper classes and include them in your project, following the procedure below.</span></span>

<span data-ttu-id="cf90a-113">**Para crear clases contenedoras e incluirlas en el proyecto**</span><span class="sxs-lookup"><span data-stu-id="cf90a-113">**To create wrapper classes and include them in your project**</span></span>

1.  <span data-ttu-id="cf90a-114">En un proyecto de Visual J++, seleccione **Agregar contenedor com...** en el menú **proyecto** .</span><span class="sxs-lookup"><span data-stu-id="cf90a-114">In a Visual J++ project, select **Add Com Wrapper...** from the **Project** menu.</span></span>
2.  <span data-ttu-id="cf90a-115">Seleccione "biblioteca de tipos Active DS" en los **componentes instalados:** en el cuadro de diálogo contenedores com.</span><span class="sxs-lookup"><span data-stu-id="cf90a-115">Select "Active DS Type Library" from the **Installed Components:** from the COM Wrappers dialog.</span></span> <span data-ttu-id="cf90a-116">Si la biblioteca de tipos no se muestra en el cuadro de lista, haga clic en el botón **examinar...** , desplácese hasta el directorio donde se almacena activeds. tlb y, a continuación, seleccione la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="cf90a-116">If the type library is not shown in the list box, click the **Browse...** button, navigate to the directory where Activeds.tlb is stored, and then select the type library.</span></span>

<span data-ttu-id="cf90a-117">Visual J++ crea el paquete activeds para las clases contenedoras de Java e incluye el paquete en la ruta de acceso predeterminada del proyecto.</span><span class="sxs-lookup"><span data-stu-id="cf90a-117">Visual J++ creates the activeds package for the Java Wrapper classes and include the package into the project's default path.</span></span> <span data-ttu-id="cf90a-118">Para obtener más información, vea el paquete activeds en el panel de **exploración del proyecto** en la ventana de Visual J++.</span><span class="sxs-lookup"><span data-stu-id="cf90a-118">For more information, see the activeds package in the **Project Explore** pane on the Visual J++ window.</span></span>

<span data-ttu-id="cf90a-119">Para obtener un objeto ADSI que no se pueda crear, use una de las funciones de la API ADSI expuestas, por ejemplo, [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) o [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), que también se empaquetan en Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="cf90a-119">To get an ADSI object that cannot be cocreated, use one of the exposed ADSI API functions, for example, [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) or [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), which are also packaged in Activeds.dll.</span></span> <span data-ttu-id="cf90a-120">Microsoft J/Direct proporciona acceso a estas y otras API nativas.</span><span class="sxs-lookup"><span data-stu-id="cf90a-120">Microsoft J/Direct provides access to these and other native APIs.</span></span> <span data-ttu-id="cf90a-121">Esto se muestra en las dos últimas líneas del ejemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="cf90a-121">This is illustrated by the last two lines of the code example, above.</span></span>

<span data-ttu-id="cf90a-122">Al compilar, asegúrese de que la extensión de idioma de Microsoft está habilitada.</span><span class="sxs-lookup"><span data-stu-id="cf90a-122">When compiling, ensure that Microsoft Language Extension is enabled.</span></span> <span data-ttu-id="cf90a-123">Para ello, seleccione **<project> propiedades...** en el menú **proyecto** de la ventana proyecto de Visual J++.</span><span class="sxs-lookup"><span data-stu-id="cf90a-123">To do this, select **<project> Properties...** from the **Project** menu in the Visual J++ project window.</span></span> <span data-ttu-id="cf90a-124">A continuación, haga clic en la pestaña **compilar** en el cuadro de diálogo **<project> propiedades** .</span><span class="sxs-lookup"><span data-stu-id="cf90a-124">Then, click the **Compile** tab in the **<project> Properties** dialog.</span></span> <span data-ttu-id="cf90a-125">Desactive la casilla **deshabilitar extensiones de lenguaje de Microsoft** .</span><span class="sxs-lookup"><span data-stu-id="cf90a-125">Clear the **Disable Microsoft Language Extensions** check box.</span></span> <span data-ttu-id="cf90a-126">Si compila desde la línea de comandos, use el modificador "/x-", por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="cf90a-126">If compiling from the command line, use "/x-" switch, for example:</span></span>

<span data-ttu-id="cf90a-127">**JVC/x-SimpleADSI. Java**</span><span class="sxs-lookup"><span data-stu-id="cf90a-127">**jvc /x- SimpleADSI.java**</span></span>

<span data-ttu-id="cf90a-128">Por último, para que la máquina virtual cargue el componente COM, la biblioteca de vínculos dinámicos (DLL) debe estar visible en la ruta de acceso del sistema.</span><span class="sxs-lookup"><span data-stu-id="cf90a-128">Finally, in order for the virtual machine to load the COM component, the dynamic-link library (DLL) must be visible on the system path.</span></span> <span data-ttu-id="cf90a-129">Si se devuelve un error "Java. lang. UnsatisfiedLinkError", establezca la ruta de acceso para incluir la ruta de acceso que contiene el archivo DLL necesario.</span><span class="sxs-lookup"><span data-stu-id="cf90a-129">If a "java.lang.UnsatisfiedLinkError" error is returned, set the PATH to include the path that contains the required DLL.</span></span> <span data-ttu-id="cf90a-130">Por ejemplo, si se ha instalado Activeds.dll en c: \\ ADSI \\ lib, emita el siguiente comando desde la línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="cf90a-130">For example, if Activeds.dll has been installed in c:\\adsi\\lib, issue the following command from the command line:</span></span>

<span data-ttu-id="cf90a-131">**establecer ruta de acceso =% PATH%; c: \\ ADSI \\ lib**</span><span class="sxs-lookup"><span data-stu-id="cf90a-131">**set PATH = %PATH%; c:\\adsi\\lib**</span></span>

 

 




