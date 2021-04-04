---
title: Detectar el maestro de esquema
description: Active Directory Domain Services tener un sistema de actualización con varios maestros; cada controlador de dominio contiene una copia de escritura del directorio.
ms.assetid: 8e096351-43f8-48ee-acb6-681d9e38e93c
ms.tgt_platform: multiple
keywords:
- Detección del anuncio maestro de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6869853cba68d7155f2091e2fe4515116944a629
ms.sourcegitcommit: f730b85cc85448913e50a7f331e10b646ea7978b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/23/2019
ms.locfileid: "103903927"
---
# <a name="detecting-the-schema-master"></a><span data-ttu-id="a1dcb-104">Detectar el maestro de esquema</span><span class="sxs-lookup"><span data-stu-id="a1dcb-104">Detecting the Schema Master</span></span>

<span data-ttu-id="a1dcb-105">Active Directory Domain Services tener un sistema de actualización con varios maestros; cada controlador de dominio contiene una copia de escritura del directorio.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-105">Active Directory Domain Services have a multi-master update system; every domain controller holds a writable copy of the directory.</span></span> <span data-ttu-id="a1dcb-106">Las actualizaciones de esquema se propagan a todos los dominios que pertenecen al mismo árbol o bosque.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-106">Schema updates are propagated to all domains that belong to the same tree or forest.</span></span> <span data-ttu-id="a1dcb-107">Dado que es difícil conciliar las actualizaciones conflictivas en el esquema, las actualizaciones de esquema solo se pueden realizar en un solo servidor.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-107">Because it is difficult to reconcile conflicting updates to the schema, schema updates can only be performed at a single server.</span></span> <span data-ttu-id="a1dcb-108">El servidor con el derecho a realizar actualizaciones puede cambiar, pero solo un servidor tendrá el derecho en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-108">The server with the right to perform updates can change, but only one server will have that right at any given time.</span></span> <span data-ttu-id="a1dcb-109">Este servidor se denomina maestro de esquema.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-109">This server is called the schema master.</span></span> <span data-ttu-id="a1dcb-110">El primer controlador de dominio instalado en una empresa es, de forma predeterminada, el maestro de esquema.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-110">The first DC installed in an enterprise is, by default, the schema master.</span></span>

<span data-ttu-id="a1dcb-111">Los cambios de esquema solo se pueden realizar en el nivel de maestro de esquema.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-111">Schema changes can only be made at the schema master level.</span></span> <span data-ttu-id="a1dcb-112">Para detectar qué controlador de dominio es el maestro de esquema, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-112">To detect which DC is the schema master, perform the following steps.</span></span>

<span data-ttu-id="a1dcb-113">**Detectar el maestro de esquema DC**</span><span class="sxs-lookup"><span data-stu-id="a1dcb-113">**Detecting the DC Schema Master**</span></span>

1.  <span data-ttu-id="a1dcb-114">Lea el atributo **fsmoRoleOwner** del contenedor de esquemas en cualquier controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-114">Read the **fsmoRoleOwner** attribute of the schema container on any DC.</span></span> <span data-ttu-id="a1dcb-115">El atributo **fsmoRoleOwner** devuelve el nombre distintivo (DN) del objeto **nTDSDSA** para el maestro de esquema.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-115">The **fsmoRoleOwner** attribute returns the distinguished name (DN) of the **nTDSDSA** object for the schema master.</span></span>
2.  <span data-ttu-id="a1dcb-116">Enlace al objeto **nTDSDSA** cuyo DN acaba de recuperar.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-116">Bind to the **nTDSDSA** object whose DN you just retrieved.</span></span> <span data-ttu-id="a1dcb-117">El elemento primario de este objeto es el objeto de servidor del controlador de dominio que contiene el maestro de esquema.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-117">The parent of this object is the server object for the DC containing the schema master.</span></span>
3.  <span data-ttu-id="a1dcb-118">Obtiene el ADsPath para el elemento primario del objeto **nTDSDSA** .</span><span class="sxs-lookup"><span data-stu-id="a1dcb-118">Get the ADsPath for the parent of the **nTDSDSA** object.</span></span> <span data-ttu-id="a1dcb-119">El elemento primario es un objeto de servidor.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-119">The parent is a server object.</span></span>
4.  <span data-ttu-id="a1dcb-120">Enlazar al objeto de servidor.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-120">Bind to the server object.</span></span>
5.  <span data-ttu-id="a1dcb-121">Obtiene el atributo **DnsHostName** del objeto de servidor.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-121">Get the **dNSHostName** attribute of the server object.</span></span> <span data-ttu-id="a1dcb-122">Es el nombre DNS del controlador de dominio que contiene el maestro de esquema.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-122">This is the DNS name of the DC that contains the schema master.</span></span>
6.  <span data-ttu-id="a1dcb-123">Especifique el nombre DNS del maestro de esquema como el servidor y el DN como el DN del contenedor de esquemas que se va a enlazar al maestro de esquema.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-123">Specify the DNS name of the schema master as the server and the DN as the DN of the schema container to bind to the schema master.</span></span> <span data-ttu-id="a1dcb-124">Por ejemplo, si el servidor era "dc1.fabrikam.com" y el DN del contenedor de esquemas fuera "CN = Schema, CN = Configuration, DC = Fabrikam, DC = com", el ADsPath sería como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-124">For example, if the server was "dc1.fabrikam.com" and the schema container DN was "cn=schema,cn=configuration,dc=fabrikam,dc=com", the ADsPath would be as follows.</span></span>
    ```C++
    LDAP://dc1.fabrikam.com/cn=schema,cn=configuration,dc=fabrikam,dc=com
    ```

    

<span data-ttu-id="a1dcb-125">Se recomienda encontrar el maestro de esquema y enlazarlo para realizar cambios en el esquema.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-125">It is recommended that you find the schema master and bind to it to make schema changes.</span></span> <span data-ttu-id="a1dcb-126">Sin embargo, puede trasladar el maestro de esquema a otro servidor.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-126">However, you can move the schema master to another server.</span></span>

<span data-ttu-id="a1dcb-127">Para convertir otro servidor en el maestro de esquema, un usuario con privilegios adecuados puede:</span><span class="sxs-lookup"><span data-stu-id="a1dcb-127">To make another server the schema master, a suitably privileged user can:</span></span>

-   <span data-ttu-id="a1dcb-128">Use el complemento MMC del administrador de esquemas.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-128">Use the Schema Manager MMC snap-in.</span></span>
    > [!Note]
    > <span data-ttu-id="a1dcb-129">El complemento MMC de esquema Active Directory debe registrarse manualmente.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-129">The Active Directory Schema MMC snap-in must be registered manually.</span></span> <span data-ttu-id="a1dcb-130">Para registrar el complemento esquema, debe ejecutar el siguiente comando desde el símbolo del sistema en el directorio system32 de Windows.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-130">To register the Schema snap-in, you must run the following command from the command prompt in the Windows System32 directory.</span></span>
    >
    > <span data-ttu-id="a1dcb-131">**regsvr32.exe schmmgmt.dll**</span><span class="sxs-lookup"><span data-stu-id="a1dcb-131">**regsvr32.exe schmmgmt.dll**</span></span>

     

-   <span data-ttu-id="a1dcb-132">Use la utilidad de línea de comandos NTDSUTIL.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-132">Use the NTDSUTIL command-line utility.</span></span>
-   <span data-ttu-id="a1dcb-133">Usar una aplicación de terceros (una aplicación que emite la escritura LDAP adecuada).</span><span class="sxs-lookup"><span data-stu-id="a1dcb-133">Use a third-party application (an application that issues the appropriate LDAP write).</span></span>

<span data-ttu-id="a1dcb-134">Para convertirse en el maestro de esquema mediante programación, una aplicación que se ejecuta en el contexto de un usuario con privilegios adecuados puede emitir una escritura LDAP del atributo operativo **becomeschemamaster.** a RootDSE en dicho controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-134">To become the schema master programmatically, an application running in the context of a suitably privileged user can issue an LDAP write of the operational attribute **becomeSchemaMaster** to the rootDSE on that DC.</span></span> <span data-ttu-id="a1dcb-135">Esto inicia una transferencia atómica del derecho del maestro de esquema desde el titular actual hasta el controlador de dominio local.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-135">This initiates an atomic transfer of the schema master right from the current holder to the local DC.</span></span>

<span data-ttu-id="a1dcb-136">En el ejemplo de código siguiente se busca el maestro de esquema.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-136">The following code example finds the schema master.</span></span> <span data-ttu-id="a1dcb-137">La función siguiente enlaza al contenedor de esquema en el equipo que es el maestro de esquema.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-137">The following function binds to the schema container on the computer that is the schema master.</span></span>


```C++
HRESULT BindToSchemaMaster(IADsContainer **ppSchemaMaster)
{
HRESULT hr = E_FAIL;
// Get rootDSE and the schema container DN.
IADs *pObject = NULL;
IADs *pTempSchema = NULL;
IADs *pNTDS = NULL;
IADs *pServer = NULL;
BSTR bstrParent;
LPOLESTR szPath = new OLECHAR[MAX_PATH];
VARIANT var, varRole,varComputer;
hr = ADsOpenObject(L"LDAP://rootDSE",
         NULL,
         NULL,
         ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
         IID_IADs,
         (void**)&pObject);
if (hr == S_OK)
{
  hr = pObject->Get(CComBSTR("schemaNamingContext"), &var);
  if (hr == S_OK)
  {
    wcscpy_s(szPath,L"LDAP://");
    wcscat_s(szPath,var.bstrVal);
    hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
             IID_IADs,
             (void**)&pTempSchema);
 
    if (hr == S_OK)
    {
      /*
      Read the fsmoRoleOwner attribute to identify which server is 
      the schema master.
      */  
      hr = pTempSchema->Get(CComBSTR("fsmoRoleOwner"), &varRole);
      if (hr == S_OK)
      {
        // The fsmoRoleOwner attribute returns the nTDSDSA object.
        // The parent is the server object.
        // Bind to NTDSDSA object and get parent.
        wcscpy_s(szPath,L"LDAP://");
        wcscat_s(szPath,varRole.bstrVal);
        hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION,
             IID_IADs,
             (void**)&pNTDS);
        if (hr == S_OK)
        {
          hr = pNTDS->get_Parent(&bstrParent);
          if (hr == S_OK)
          {
            /*
            Bind to server object and get the DNS name of 
            the server.
            */
            wcscpy_s(szPath,bstrParent);
            hr = ADsOpenObject(szPath,
               NULL,
               NULL,
               ADS_SECURE_AUTHENTICATION,
               IID_IADs,
               (void**)&pServer);
            if (hr == S_OK)
            {
              // Get the dns name of the server.
              hr = pServer->Get(CComBSTR("dNSHostName"), 
                  &varComputer);
              if (hr == S_OK)
              {
                    wcscpy_s(szPath,L"LDAP://");
                    wcscat_s(szPath,varComputer.bstrVal);
                    wcscat_s(szPath,L"/");
                    wcscat_s(szPath,var.bstrVal);
                    hr = ADsOpenObject(szPath,
                         NULL,
                         NULL,
                         ADS_SECURE_AUTHENTICATION,
                         IID_IADs,
                         (void**)ppSchemaMaster);
                    if (FAILED(hr))
                    {
                      if (*ppSchemaMaster)
                      {
                        (*ppSchemaMaster)->Release();
                        (*ppSchemaMaster) = NULL;
                      }
                    }
              }
              VariantClear(&varComputer);
            }
            if (pServer)
              pServer->Release();
          }
          SysFreeString(bstrParent);
        }
        if (pNTDS)
          pNTDS->Release();
      }
      VariantClear(&varRole);
    }
    if (pTempSchema)
      pTempSchema->Release();
  }
  VariantClear(&var);
}
if (pObject)
    pObject->Release();
 
return hr;
}
```



<span data-ttu-id="a1dcb-138">En el ejemplo de código siguiente se muestra el nombre DNS del equipo que es el maestro de esquema.</span><span class="sxs-lookup"><span data-stu-id="a1dcb-138">The following code example displays the DNS name for the computer that is the schema master.</span></span>


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
''''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the schema
''''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the schema container
''''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the 
' schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' The fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get the parent object.
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("dNSHostName")
''''''''''''''''''''
' Display the DNS name for the computer.
''''''''''''''''''''
strText = "Schema master has the following DNS name: "& sComputer
WScript.echo strText
 
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)
    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 




