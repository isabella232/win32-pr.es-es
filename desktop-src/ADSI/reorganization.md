---
title: Reorganización
description: La organización de ventas se ha migrado a una nueva organización \ 8212; \ 0034; Ventas y soporte técnico. \ 0034; Julia Bankert se ha promocionado al Vicepresidente y liderará la nueva organización.
ms.assetid: 38b05d0b-2739-43c2-aac7-7555a5bfbc91
ms.tgt_platform: multiple
keywords:
- Reorganización ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587f3de34738814b34ad250bb00bb7b71121d65c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075067"
---
# <a name="reorganization"></a><span data-ttu-id="271a2-105">Reorganización</span><span class="sxs-lookup"><span data-stu-id="271a2-105">Reorganization</span></span>

<span data-ttu-id="271a2-106">La organización de ventas se ha migrado a una nueva organización, "ventas y soporte técnico".</span><span class="sxs-lookup"><span data-stu-id="271a2-106">The sales organization has moved to a new organization — "Sales and Support."</span></span> <span data-ttu-id="271a2-107">Julia Bankert se ha promocionado al Vicepresidente y liderará la nueva organización.</span><span class="sxs-lookup"><span data-stu-id="271a2-107">Julie Bankert has been promoted to vice president and will lead the new organization.</span></span> <span data-ttu-id="271a2-108">Joe Worden, el administrador de la empresa, debe trasladar las unidades organizativas de ventas a una nueva unidad organizativa, ventas y soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="271a2-108">Joe Worden, the enterprise administrator, must move Sales OU to a new OU, Sales and Support.</span></span>


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=COM")
Set salesSupport = dom.Create("organizationalUnit", "CN=Sales and Support")
Set sales = salesSupport.MoveHere("LDAP://OU=Sales,DC=Fabrikam,DC=COM", vbNullString)
```



<span data-ttu-id="271a2-109">Con este ejemplo de código, todos los objetos de la unidad organizativa sales, incluidas las unidades organizativas, se mueven a la nueva unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="271a2-109">With this code example, all objects in the sales organizational unit, including the sub-organizational units, are moved to the new organizational unit.</span></span>

<span data-ttu-id="271a2-110">Ahora, Joe puede trasladar Julia a la unidad organizativa de ventas y soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="271a2-110">Now, Joe can move Julie into the Sales and Support organizational unit.</span></span>


```VB
Set usr = salesSupport.MoveHere("LDAP://CN=Julie Bankert,OU=Sales,OU=Sales and Support,DC=Fabrikam,DC=COM")
usr.Put "title", "Vice President"
usr.SetInfo
```



<span data-ttu-id="271a2-111">Tenga en cuenta que el vínculo de informe Director-directo entre Julia Bankert y Chris Gray se actualiza automáticamente mediante Active Directory.</span><span class="sxs-lookup"><span data-stu-id="271a2-111">Be aware that the manager-direct report link between Julie Bankert and Chris Gray is automatically updated by Active Directory.</span></span>

<span data-ttu-id="271a2-112">**Para crear un informe de Active Directory**</span><span class="sxs-lookup"><span data-stu-id="271a2-112">**To create an Active Directory report**</span></span>

1.  <span data-ttu-id="271a2-113">Abra Visual Basic versión 6,0 y, cuando se le pida el tipo de proyecto, seleccione **proyecto de datos**.</span><span class="sxs-lookup"><span data-stu-id="271a2-113">Open Visual Basic version 6.0, and when prompted for the project type, select **Data Project**.</span></span>
2.  <span data-ttu-id="271a2-114">En **proyecto de datos**, haga doble clic en **Environment1 de datos**.</span><span class="sxs-lookup"><span data-stu-id="271a2-114">On **Data Project**, double-click **Data Environment1**.</span></span>
3.  <span data-ttu-id="271a2-115">En la ventana **entorno de datos** , haga clic con el botón secundario en el objeto de conexión **(Connection1)** y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="271a2-115">On the **Data Environment** window, right-click the connection object **(Connection1)** and select **Properties**.</span></span>
4.  <span data-ttu-id="271a2-116">Seleccione **proveedor de OLE DB para servicios de directorio de Microsoft** y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="271a2-116">Select **OLE DB Provider for Microsoft Directory Services**, and click **Next**.</span></span>
5.  <span data-ttu-id="271a2-117">Seleccione **usar seguridad integrada de Windows NT** y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="271a2-117">Select **Use Windows NT Integrated security**, and click **OK**.</span></span> <span data-ttu-id="271a2-118">Esto crea un objeto de conexión.</span><span class="sxs-lookup"><span data-stu-id="271a2-118">This creates a connection object.</span></span>
6.  <span data-ttu-id="271a2-119">Vuelva a hacer clic con el botón secundario en la ventana del **entorno de datos** para seleccionar **Agregar comando**.</span><span class="sxs-lookup"><span data-stu-id="271a2-119">Right-click the **Data Environment** window again to select **Add Command**.</span></span> <span data-ttu-id="271a2-120">Haga clic con el botón secundario en el objeto **Command1** y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="271a2-120">Right-click the **Command1** object and select **Properties**.</span></span> <span data-ttu-id="271a2-121">Aparecerá el siguiente cuadro de diálogo **propiedades de Command1** .</span><span class="sxs-lookup"><span data-stu-id="271a2-121">The following **Command1 Properties** dialog box will appear.</span></span>

    ![cuadro de diálogo Propiedades de Command1](images/adadsi3.png)

7.  <span data-ttu-id="271a2-123">Haga clic en el botón de opción **instrucción SQL** y escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="271a2-123">Click the **SQL Statement** option button and type the following:</span></span>

    <span data-ttu-id="271a2-124">Seleccione Name, telephoneNumber de ' LDAP://DC = Fabrikam, DC = com ', donde objectCategory = ' Person ' y objectClass = ' User '</span><span class="sxs-lookup"><span data-stu-id="271a2-124">SELECT Name,telephoneNumber FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectCategory='Person' AND objectClass='user'</span></span>

    <span data-ttu-id="271a2-125">Se crea el objeto de **comando** .</span><span class="sxs-lookup"><span data-stu-id="271a2-125">The **Command** object is created.</span></span> <span data-ttu-id="271a2-126">Agregue el objeto de **comando** al informe.</span><span class="sxs-lookup"><span data-stu-id="271a2-126">Add the **Command** object to the report.</span></span>

8.  <span data-ttu-id="271a2-127">Haga doble clic en **Data informe1** en la ventana **proyecto** .</span><span class="sxs-lookup"><span data-stu-id="271a2-127">Double-click **Data Report1** from the **Project** window.</span></span>
9.  <span data-ttu-id="271a2-128">Arrastre el objeto **Command1** desde la ventana **DataEnvironment1** a la sección de **detalles** de la ventana de **Informe de datos** .</span><span class="sxs-lookup"><span data-stu-id="271a2-128">Drag the **Command1** object from the **DataEnvironment1** window to the **Detail** section in the **Data Report** window.</span></span>
10. <span data-ttu-id="271a2-129">En **propiedades de DataReport1**, en **DataSource**, seleccione **DataEnvironment1** en el menú desplegable y seleccione **Command1** en el campo **DataMember** .</span><span class="sxs-lookup"><span data-stu-id="271a2-129">On **DataReport1 Properties**, for **DataSource**, select **DataEnvironment1** from the pull-down menu, and select **Command1** in the **DataMember** field.</span></span>
11. <span data-ttu-id="271a2-130">En la ventana proyecto, haga clic con el botón derecho en **proyecto de datos** y seleccione **propiedades de proyecto**.</span><span class="sxs-lookup"><span data-stu-id="271a2-130">On the project window, right-click **Data Project**, and select **DataProject Properties**.</span></span>
12. <span data-ttu-id="271a2-131">En el cuadro de diálogo Propiedades de proyecto de **proyecto** , en **objeto de inicio**, seleccione **DataReport1** en el menú desplegable.</span><span class="sxs-lookup"><span data-stu-id="271a2-131">On the **DataProject - Project Properties** dialog window, under **Startup Object**, select **DataReport1** from the pull-down menu.</span></span> <span data-ttu-id="271a2-132">Haz clic en **Aceptar** para guardar.</span><span class="sxs-lookup"><span data-stu-id="271a2-132">Click **OK** to save.</span></span>
13. <span data-ttu-id="271a2-133">Compilación.</span><span class="sxs-lookup"><span data-stu-id="271a2-133">Compile.</span></span> <span data-ttu-id="271a2-134">Aparecerá el siguiente cuadro de diálogo **DataReport1** .</span><span class="sxs-lookup"><span data-stu-id="271a2-134">The following **DataReport1** dialog box will appear.</span></span>

    ![cuadro de diálogo datareport1](images/adadsi4.png)

## <a name="related-topics"></a><span data-ttu-id="271a2-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="271a2-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="271a2-137">Combinar datos heterogéneos</span><span class="sxs-lookup"><span data-stu-id="271a2-137">Joining Heterogeneous Data</span></span>](joining-heterogeneous-data.md)
</dt> </dl>

 

 




