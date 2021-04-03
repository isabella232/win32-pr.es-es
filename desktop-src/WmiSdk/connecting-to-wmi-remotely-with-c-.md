---
description: Como con otros lenguajes como PowerShell, VBScript o C++, puede usar C# para supervisar de forma remota el hardware y el software de los equipos remotos.
ms.assetid: 9E03A8D0-01AB-4B7E-99B6-FEEF9C1CAE17
ms.tgt_platform: multiple
title: 'Conexión a WMI de forma remota con C #'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2ad9fe2008b52276a8f68149b33ae3729daaf7d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083073"
---
# <a name="connecting-to-wmi-remotely-with-c"></a><span data-ttu-id="b8d0b-103">Conexión a WMI de forma remota con C #</span><span class="sxs-lookup"><span data-stu-id="b8d0b-103">Connecting to WMI Remotely with C#</span></span>

<span data-ttu-id="b8d0b-104">Como con otros lenguajes como PowerShell, VBScript o C++, puede usar C# para supervisar de forma remota el hardware y el software de los equipos remotos.</span><span class="sxs-lookup"><span data-stu-id="b8d0b-104">As with other languages such as PowerShell, VBScript, or C++, you can use C# to remotely monitor the hardware and software on remote computers.</span></span> <span data-ttu-id="b8d0b-105">Las conexiones remotas para código administrado se realizan a través del espacio de nombres [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b8d0b-105">Remote connections for managed code are accomplished through the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace.</span></span> <span data-ttu-id="b8d0b-106">(Las versiones anteriores de WMI usaban el espacio de nombres [System. Management](/dotnet/api/system.management) , que se incluye aquí para integridad).</span><span class="sxs-lookup"><span data-stu-id="b8d0b-106">(Previous versions of WMI used the [System.Management](/dotnet/api/system.management) namespace, which is included here for completeness.)</span></span>

> [!Note]  
> <span data-ttu-id="b8d0b-107">**System. Management** era el espacio de nombres .net original utilizado para tener acceso a WMI. sin embargo, las API de este espacio de nombres suelen ser más lentas y no se escalan con respecto a sus homólogos de **Microsoft. Management. Infrastructure** más modernos.</span><span class="sxs-lookup"><span data-stu-id="b8d0b-107">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="b8d0b-108">La conexión remota mediante las clases del espacio de nombres [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) usa DCOM como mecanismo remoto subyacente.</span><span class="sxs-lookup"><span data-stu-id="b8d0b-108">Connecting remotely using classes in the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace uses DCOM as the underlying remote mechanism.</span></span> <span data-ttu-id="b8d0b-109">Las conexiones WMI remotas se deben ajustar a los requisitos de seguridad de DCOM en lo que respecta a la suplantación y la autenticación.</span><span class="sxs-lookup"><span data-stu-id="b8d0b-109">WMI remote connections must comply with DCOM security requirements for impersonation and authentication.</span></span> <span data-ttu-id="b8d0b-110">De forma predeterminada, un ámbito está enlazado al equipo local y al \\ espacio de nombres del sistema "root CIMv2".</span><span class="sxs-lookup"><span data-stu-id="b8d0b-110">By default, a scope is bound to the local computer and the "Root\\CIMv2" system namespace.</span></span> <span data-ttu-id="b8d0b-111">Sin embargo, puede cambiar el equipo, el dominio y el espacio de nombres WMI al que tiene acceso.</span><span class="sxs-lookup"><span data-stu-id="b8d0b-111">However, you can change both the computer, domain, and WMI namespace that you access.</span></span> <span data-ttu-id="b8d0b-112">También puede establecer la autoridad, la suplantación, las credenciales y otras opciones de conexión.</span><span class="sxs-lookup"><span data-stu-id="b8d0b-112">You can also set authority, impersonation, credentials, and other connection options.</span></span>

<span data-ttu-id="b8d0b-113">**Para conectarse a WMI de forma remota con C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="b8d0b-113">**To connect to WMI remotely with C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="b8d0b-114">Cree una sesión en el equipo remoto con una llamada a [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b8d0b-114">Create a session on the remote machine with a call to [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)).</span></span>

    <span data-ttu-id="b8d0b-115">Si se va a conectar a un equipo remoto con las mismas credenciales (dominio y nombre de usuario) con la que ha iniciado sesión, puede especificar el nombre del equipo en la llamada de [creación](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b8d0b-115">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you can specify the name of the computer in the [Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) call.</span></span> <span data-ttu-id="b8d0b-116">Una vez que tenga el objeto [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) devuelto, puede realizar la consulta de WMI.</span><span class="sxs-lookup"><span data-stu-id="b8d0b-116">Once you have the returned [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object, you can then make your WMI query.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string OSQuery = "SELECT * FROM Win32_OperatingSystem";
    CimSession mySession = CimSession.Create("Computer_B");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
    ```

    

    <span data-ttu-id="b8d0b-117">Para obtener más información sobre cómo realizar consultas WMI con la API **Microsoft. Management. Infrastructure** en C#, vea [recuperar datos de clase o instancia de WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="b8d0b-117">For more information on making WMI queries with the **Microsoft.Management.Infrastructure** API in C#, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="b8d0b-118">Si desea establecer diferentes opciones para la conexión, como las distintas credenciales, la configuración regional o los niveles de suplantación, debe usar un objeto [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) en la llamada a [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b8d0b-118">If you wish to set different options for your connection, such as different credentials, locale or Impersonation levels, you need to use a [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) object in your call to [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)).</span></span>

    <span data-ttu-id="b8d0b-119">[CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) es una clase base para [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) y [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b8d0b-119">[CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) is a base class for [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) and [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)).</span></span> <span data-ttu-id="b8d0b-120">Puede usar o para establecer las opciones de las sesiones de WS-Man y DCOM, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b8d0b-120">You can use either to set the options on your WS-Man and DCOM sessions, respectively.</span></span> <span data-ttu-id="b8d0b-121">En el ejemplo de código siguiente se describe el uso de un objeto [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) para establecer el nivel de suplantación en Impersonate.</span><span class="sxs-lookup"><span data-stu-id="b8d0b-121">The following code sample describes using a [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) object to set the Impersonation level to Impersonate.</span></span>

    ```CSharp
    string computer = "Computer_B"
    DComSessionOptions DComOptions = new DComSessionOptions();
    DComOptions.Impersonation = ImpersonationType.Impersonate;

    CimSession Session = CimSession.Create(computer, DComOptions);
    ```

    

3.  <span data-ttu-id="b8d0b-122">Si desea establecer las credenciales para la conexión, tendrá que crear y agregar un objeto [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) a [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b8d0b-122">If you wish to set the credentials for your connection, you will need to create and add a [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) object to your [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)).</span></span>

    <span data-ttu-id="b8d0b-123">En el ejemplo de código siguiente se describe cómo crear una clase [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) , rellenarla con el [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))adecuado y usarla en una llamada [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b8d0b-123">The following code sample describes creating a [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) class, filling it with the proper [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)), and using it in a [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) call.</span></span>

    ```CSharp
    string computer = “Computer_B”;
    string domain = “Domain1″;
    string username = “User1″;

    string plaintextpassword; 

    //Retrieve password from the user. 
    //For the complete code, see the sample at the bottom of this topic.

    CimCredential Credentials = new CimCredential(PasswordAuthenticationMechanism.Default, domain, username, securepassword); 

    WSManSessionOptions SessionOptions = new WSManSessionOptions();
    SessionOptions.AddDestinationCredentials(Credentials); 

    CimSession Session = CimSession.Create(computer, SessionOptions);
    ```

    

    <span data-ttu-id="b8d0b-124">Por lo general, se recomienda no codificar una contraseña en las aplicaciones; como indica el ejemplo de código anterior, siempre que sea posible, intente consultar a su usuario la contraseña y guárdela de forma segura.</span><span class="sxs-lookup"><span data-stu-id="b8d0b-124">It is generally recommended that you do not hardcode a password into your applications; as the above code sample indicates, whenever possible try to query your user for the password, and store it securely.</span></span>

<span data-ttu-id="b8d0b-125">WMI está diseñado para supervisar el hardware y el software en equipos remotos.</span><span class="sxs-lookup"><span data-stu-id="b8d0b-125">WMI is intended to monitor the hardware and software on remote computers.</span></span> <span data-ttu-id="b8d0b-126">Las conexiones remotas para WMI v1 se realizan a través del objeto [ManagementScope](/dotnet/api/system.management.managementscope) .</span><span class="sxs-lookup"><span data-stu-id="b8d0b-126">Remote connections for WMI v1 is accomplished through the [ManagementScope](/dotnet/api/system.management.managementscope) object.</span></span>

<span data-ttu-id="b8d0b-127">**Para conectarse a WMI de forma remota con C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="b8d0b-127">**To connect to WMI remotely with C# (System.Management)**</span></span>

1.  <span data-ttu-id="b8d0b-128">Cree un objeto [ManagementScope](/dotnet/api/system.management.managementscope) , utilizando el nombre del equipo y la ruta de acceso WMI, y conéctese a su destino con una llamada a ManagementScope. Connect ().</span><span class="sxs-lookup"><span data-stu-id="b8d0b-128">Create a [ManagementScope](/dotnet/api/system.management.managementscope) object, using the name of the computer and the WMI path, and connect to your target with a call to ManagementScope.Connect().</span></span>

    <span data-ttu-id="b8d0b-129">Si se va a conectar a un equipo remoto con las mismas credenciales (dominio y nombre de usuario) con la que ha iniciado sesión, solo tendrá que especificar la ruta de acceso WMI.</span><span class="sxs-lookup"><span data-stu-id="b8d0b-129">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you only have to specify the WMI path.</span></span> <span data-ttu-id="b8d0b-130">Una vez que se haya conectado, puede realizar la consulta de WMI.</span><span class="sxs-lookup"><span data-stu-id="b8d0b-130">Once you have connected, you can make your WMI query.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
    scope.Connect();
    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
    ```

    

    <span data-ttu-id="b8d0b-131">Para obtener más información sobre cómo realizar consultas WMI con la API [System. Management](/dotnet/api/system.management) en C#, vea [recuperar datos de clase o instancia de WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="b8d0b-131">For more information on making WMI queries with the [System.Management](/dotnet/api/system.management) API in C#, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="b8d0b-132">Si se conecta a un equipo remoto en un dominio diferente o usa un nombre de usuario y una contraseña diferentes, debe usar un objeto [ConnectionOptions](/dotnet/api/system.management.connectionoptions) en la llamada a [ManagementScope](/dotnet/api/system.management.managementscope).</span><span class="sxs-lookup"><span data-stu-id="b8d0b-132">If you connect to a remote computer in a different domain or using a different user name and password, then you must use a [ConnectionOptions](/dotnet/api/system.management.connectionoptions) object in the call to the [ManagementScope](/dotnet/api/system.management.managementscope).</span></span>

    <span data-ttu-id="b8d0b-133">[ConnectionOptions](/dotnet/api/system.management.connectionoptions) contiene propiedades para describir la autenticación, la suplantación, el nombre de usuario, la contraseña y otras opciones de conexión.</span><span class="sxs-lookup"><span data-stu-id="b8d0b-133">The [ConnectionOptions](/dotnet/api/system.management.connectionoptions) contains properties for describing the Authentication, Impersonation, username, password, and other connection options.</span></span> <span data-ttu-id="b8d0b-134">En el ejemplo de código siguiente se describe el uso de [ConnectionOptions](/dotnet/api/system.management.connectionoptions) para establecer el nivel de suplantación en Impersonate.</span><span class="sxs-lookup"><span data-stu-id="b8d0b-134">The following code sample describes using a [ConnectionOptions](/dotnet/api/system.management.connectionoptions) to set the Impersonation Level to Impersonate.</span></span>

    ```CSharp
    ConnectionOptions options = new ConnectionOptions();
    options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

    ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
    scope.Connect();

    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);
    ```

    

    <span data-ttu-id="b8d0b-135">En general, se recomienda establecer el nivel de suplantación en Impersonate, a menos que se necesite explícitamente.</span><span class="sxs-lookup"><span data-stu-id="b8d0b-135">Generally speaking, it is recommended that you set your Impersonation level to Impersonate unless explicitly needed otherwise.</span></span> <span data-ttu-id="b8d0b-136">Además, intente evitar escribir su nombre y contraseña en código C#.</span><span class="sxs-lookup"><span data-stu-id="b8d0b-136">Further, try to avoid writing your name and password into C# code.</span></span> <span data-ttu-id="b8d0b-137">(Si es posible, consulte si puede consultar al usuario para que los suministre dinámicamente en tiempo de ejecución).</span><span class="sxs-lookup"><span data-stu-id="b8d0b-137">(If possible, see if you can query the user to dynamically supply them at runtime.)</span></span>

    <span data-ttu-id="b8d0b-138">Para obtener más ejemplos de configuración de distintas propiedades en una conexión WMI remota, consulte la sección ejemplos de la página de referencia de [ConnectionOptions](/dotnet/api/system.management.connectionoptions) .</span><span class="sxs-lookup"><span data-stu-id="b8d0b-138">For more examples of setting different properties on a remote WMI connection, see the Examples section of the [ConnectionOptions](/dotnet/api/system.management.connectionoptions) reference page.</span></span>

## <a name="microsoftmanagementinfrastructure-example"></a><span data-ttu-id="b8d0b-139">Ejemplo de Microsoft. Management. Infrastructure</span><span class="sxs-lookup"><span data-stu-id="b8d0b-139">Microsoft.Management.Infrastructure Example</span></span>

<span data-ttu-id="b8d0b-140">En el siguiente ejemplo de código de C#, basado en la siguiente [entrada de blog de TechNet](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage), se describe cómo usar [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) y [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) para establecer credenciales en una conexión remota.</span><span class="sxs-lookup"><span data-stu-id="b8d0b-140">The following C# code example, based on the following [blog post on TechNet](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage), describes how to use [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) and [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) to set credentials on a remote connection.</span></span>


```CSharp
using System;
using System.Text;
using System.Threading;
using Microsoft.Management.Infrastructure;
using Microsoft.Management.Infrastructure.Options;
using System.Security; 

namespace SMAPIQuery
{
    class Program
    {
        static void Main(string[] args)
        { 

            string computer = "Computer_B";
            string domain = "DOMAIN";
            string username = "AdminUserName";


            string plaintextpassword; 

            Console.WriteLine("Enter password:");
            plaintextpassword = Console.ReadLine(); 

            SecureString securepassword = new SecureString();
            foreach (char c in plaintextpassword)
            {
                securepassword.AppendChar(c);
            } 

            // create Credentials
            CimCredential Credentials = new CimCredential(PasswordAuthenticationMechanism.Default, 
                                                          domain, 
                                                          username, 
                                                          securepassword); 

            // create SessionOptions using Credentials
            WSManSessionOptions SessionOptions = new WSManSessionOptions();
            SessionOptions.AddDestinationCredentials(Credentials); 

            // create Session using computer, SessionOptions
            CimSession Session = CimSession.Create(computer, SessionOptions); 

            var allVolumes = Session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Volume");
            var allPDisks = Session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_DiskDrive"); 

            // Loop through all volumes
            foreach (CimInstance oneVolume in allVolumes)
            {
                // Show volume information

                if (oneVolume.CimInstanceProperties["DriveLetter"].ToString()[0] > ' '  )
                {
                    Console.WriteLine("Volume ‘{0}’ has {1} bytes total, {2} bytes available", 
                                      oneVolume.CimInstanceProperties["DriveLetter"], 
                                      oneVolume.CimInstanceProperties["Size"], 
                                      oneVolume.CimInstanceProperties["SizeRemaining"]);
                }

            } 

            // Loop through all physical disks
            foreach (CimInstance onePDisk in allPDisks)
            {
                // Show physical disk information
                Console.WriteLine("Disk {0} is model {1}, serial number {2}", 
                                  onePDisk.CimInstanceProperties["DeviceId"], 
                                  onePDisk.CimInstanceProperties["Model"].ToString().TrimEnd(), 
                                  onePDisk.CimInstanceProperties["SerialNumber"]);
            } 

            Console.ReadLine();
         }
     }
 }
```



## <a name="systemmanagement-example"></a><span data-ttu-id="b8d0b-141">Ejemplo de System. Management</span><span class="sxs-lookup"><span data-stu-id="b8d0b-141">System.Management Example</span></span>

<span data-ttu-id="b8d0b-142">En el ejemplo de código de C# siguiente se describe una conexión remota general, mediante los objetos System. Management.</span><span class="sxs-lookup"><span data-stu-id="b8d0b-142">The following C# code sample describes a general remote connection, using the System.Management objects.</span></span>


```CSharp
using System;
using System.Management;
public class RemoteConnect 
{
    public static void Main() 
    {
        ConnectionOptions options = new ConnectionOptions();
        options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

        
        ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
        scope.Connect();

        //Query system for Operating System information
        ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
        ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);

        ManagementObjectCollection queryCollection = searcher.Get();
        foreach ( ManagementObject m in queryCollection)
        {
            // Display the remote computer information
            Console.WriteLine("Computer Name     : {0}", m["csname"]);
            Console.WriteLine("Windows Directory : {0}", m["WindowsDirectory"]);
            Console.WriteLine("Operating System  : {0}", m["Caption"]);
            Console.WriteLine("Version           : {0}", m["Version"]);
            Console.WriteLine("Manufacturer      : {0}", m["Manufacturer"]);
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="b8d0b-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b8d0b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8d0b-144">Conexión a WMI en un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="b8d0b-144">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
