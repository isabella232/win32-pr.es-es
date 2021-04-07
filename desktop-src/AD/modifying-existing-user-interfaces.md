---
title: Modificación de las interfaces de usuario existentes
description: En el panel de resultados del complemento MMC de usuarios y equipos de Active Directory se muestran varias columnas de datos de atributos para los objetos de un contenedor, como los atributos name y Description.
ms.assetid: 55f4ae82-c380-42a9-beba-047ffd0131eb
ms.tgt_platform: multiple
keywords:
- Modificación de las interfaces de usuario existentes AD
- Complemento usuarios y equipos de AD, modificar pantalla
- Complemento usuarios y equipos de AD, Agregar columnas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0765988a9ceed3e98966091ad94b868b96fd88
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903105"
---
# <a name="modifying-existing-user-interfaces"></a><span data-ttu-id="f1e60-106">Modificación de las interfaces de usuario existentes</span><span class="sxs-lookup"><span data-stu-id="f1e60-106">Modifying Existing User Interfaces</span></span>

<span data-ttu-id="f1e60-107">En el panel de resultados del complemento MMC de usuarios y equipos de Active Directory se muestran varias columnas de datos de atributos para los objetos de un contenedor, como los atributos **Name** y **Description** .</span><span class="sxs-lookup"><span data-stu-id="f1e60-107">The results pane of the Active Directory Users and Computers MMC snap-in displays several columns of attribute data for objects within a container, such as the **Name** and **Description** attributes.</span></span> <span data-ttu-id="f1e60-108">El complemento permite al usuario agregar y quitar las columnas que se muestran en el panel de resultados del complemento.</span><span class="sxs-lookup"><span data-stu-id="f1e60-108">The snap-in enables the user to add and remove the columns displayed in the results pane of the snap-in.</span></span>

<span data-ttu-id="f1e60-109">Para cambiar la pantalla, el usuario utiliza el menú desplegable **Ver** y selecciona **Agregar o quitar columnas**.</span><span class="sxs-lookup"><span data-stu-id="f1e60-109">To change the display, the user uses the **View** pull-down menu and selects **Add/Remove Columns**.</span></span> <span data-ttu-id="f1e60-110">En el cuadro de diálogo **Agregar o quitar columnas** , hay una lista de columnas que el usuario puede elegir para que se muestren en el panel de resultados.</span><span class="sxs-lookup"><span data-stu-id="f1e60-110">In the **Add/Remove Columns** dialog box, there is a list of columns that the user can choose from to display in the results pane.</span></span>

<span data-ttu-id="f1e60-111">El complemento MMC de Active Directory usuarios y equipos que se incluye con Windows Server 2003, Standard Edition, Windows Server 2003, Enterprise Edition y Windows Server 2003, Datacenter Edition, proporciona la capacidad de modificar la lista de columnas que se pueden mostrar en el panel de resultados del complemento de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="f1e60-111">The Active Directory Users and Computers MMC snap-in that is included with Windows Server 2003, Standard Edition, Windows Server 2003, Enterprise Edition, and Windows Server 2003, Datacenter Edition, provides the ability to modify the list of columns that can be displayed in the results pane of the snap-in for a container.</span></span> <span data-ttu-id="f1e60-112">Esta característica solo existe si el complemento está destinado a un bosque con el esquema de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f1e60-112">This feature only exists if the snap-in is targeted at a forest with Windows Server 2003 schema.</span></span>

<span data-ttu-id="f1e60-113">Para agregar una columna a la lista, agregue un valor al atributo **Extracolumns** del especificador de presentación para el tipo de objeto al que está asociado el atributo.</span><span class="sxs-lookup"><span data-stu-id="f1e60-113">To add a column to the list, add a value to the **extraColumns** attribute of the display specifier for the object type that the attribute is associated with.</span></span> <span data-ttu-id="f1e60-114">El atributo **Extracolumns** es un atributo de cadena de varios valores donde cada cadena tiene el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="f1e60-114">The **extraColumns** attribute is a multi-valued string attribute where each string is in the following format.</span></span>


```C++

<ldapdisplayname>,<column header>,<default visibility>,<width>,<unused>

```



<span data-ttu-id="f1e60-115">En la tabla siguiente se muestra el contenido de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f1e60-115">The following table lists the contents of these values.</span></span>



| <span data-ttu-id="f1e60-116">Value</span><span class="sxs-lookup"><span data-stu-id="f1e60-116">Value</span></span>                        | <span data-ttu-id="f1e60-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1e60-117">Description</span></span>                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e60-118">" &lt; LDAPDisplayName &gt; "</span><span class="sxs-lookup"><span data-stu-id="f1e60-118">"&lt;ldapdisplayname&gt;"</span></span>    | <span data-ttu-id="f1e60-119">Contiene una cadena que representa el **LDAPDisplayName** del atributo.</span><span class="sxs-lookup"><span data-stu-id="f1e60-119">Contains a string that represents the **ldapDisplayName** of the attribute.</span></span>                                                         |
| <span data-ttu-id="f1e60-120">" &lt; encabezado de columna &gt; "</span><span class="sxs-lookup"><span data-stu-id="f1e60-120">"&lt;column header&gt;"</span></span>      | <span data-ttu-id="f1e60-121">Contiene una cadena que representa el texto que se muestra en el encabezado de la columna.</span><span class="sxs-lookup"><span data-stu-id="f1e60-121">Contains a string that represents the text displayed in the header for the column.</span></span>                                                  |
| <span data-ttu-id="f1e60-122">" &lt; visibilidad predeterminada &gt; "</span><span class="sxs-lookup"><span data-stu-id="f1e60-122">"&lt;default visibility&gt;"</span></span> | <span data-ttu-id="f1e60-123">Contiene un valor numérico que es 0 si el atributo está oculto de forma predeterminada o 1 si el atributo es visible de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f1e60-123">Contains a numeric value that is 0 if the attribute is hidden by default or 1 if the attribute is visible by default.</span></span>               |
| <span data-ttu-id="f1e60-124">" &lt; width &gt; "</span><span class="sxs-lookup"><span data-stu-id="f1e60-124">"&lt;width&gt;"</span></span>              | <span data-ttu-id="f1e60-125">Contiene el ancho de la columna, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="f1e60-125">Contains the width of the column, in pixels.</span></span> <span data-ttu-id="f1e60-126">Si este valor es-1, el ancho de la columna se establece en el ancho del encabezado de columna.</span><span class="sxs-lookup"><span data-stu-id="f1e60-126">If this value is -1, the width of the column is set to the width of the column header.</span></span> |
| <span data-ttu-id="f1e60-127">" &lt; sin usar &gt; "</span><span class="sxs-lookup"><span data-stu-id="f1e60-127">"&lt;unused&gt;"</span></span>             | <span data-ttu-id="f1e60-128">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="f1e60-128">Unused.</span></span> <span data-ttu-id="f1e60-129">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f1e60-129">Must be zero.</span></span>                                                                                                               |



 

<span data-ttu-id="f1e60-130">Por ejemplo, para agregar una columna que mostrará el nombre canónico de los objetos en una unidad organizativa, se agrega un valor para el atributo **canonicalName** al atributo **extracolumns** del objeto **organizationalUnit-display** en el contenedor de especificadores de presentación.</span><span class="sxs-lookup"><span data-stu-id="f1e60-130">For example, to add a column that will display the canonical name for objects in an organizational unit, a value for the **canonicalName** attribute is added to the **extraColumns** attribute of the **organizationalUnit-Display** object in the display specifiers container.</span></span> <span data-ttu-id="f1e60-131">La cadena agregada al atributo **Extracolumns** del objeto **organizationalUnit-display** tendrá un aspecto similar al siguiente.</span><span class="sxs-lookup"><span data-stu-id="f1e60-131">The string added to the **extraColumns** attribute of the **organizationalUnit-Display** object will look like the following.</span></span>


```C++
canonicalName,Canonical Name,0,150,0
```



<span data-ttu-id="f1e60-132">En el cuadro de diálogo **Agregar o quitar columnas** solo se muestran las columnas contenidas en el atributo **extracolumns** del objeto **displaySpecifier** del tipo de contenedor que se está mostrando.</span><span class="sxs-lookup"><span data-stu-id="f1e60-132">The **Add/Remove Columns** dialog box displays only the columns that are contained in the **extraColumns** attribute of the **displaySpecifier** object of the container type that is being displayed.</span></span> <span data-ttu-id="f1e60-133">Si el atributo **Extracolumns** no contiene ningún valor, el cuadro de diálogo **Agregar o quitar columnas** mostrará un conjunto fijo de columnas.</span><span class="sxs-lookup"><span data-stu-id="f1e60-133">If the **extraColumns** attribute does not contain any values, the **Add/Remove Columns** dialog box will display a fixed set of columns.</span></span> <span data-ttu-id="f1e60-134">En el atributo **Extracolumns** del objeto de **visualización predeterminado** se incluye una copia del conjunto fijo de columnas.</span><span class="sxs-lookup"><span data-stu-id="f1e60-134">A copy of the fixed set of columns is contained in the **extraColumns** attribute of the **default-Display** object.</span></span>

<span data-ttu-id="f1e60-135">Para agregar una o más columnas a la lista de columnas de un objeto específico, debe copiar todos los valores de **Extracolumns** del objeto de **visualización predeterminado** en el objeto de destino y, a continuación, agregar las columnas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="f1e60-135">To add one or more columns to the list of columns for a specific object, you must copy all of the **extraColumns** values from the **default-Display** object to the target object and then add the custom columns.</span></span> <span data-ttu-id="f1e60-136">Si especifica el atributo **Extracolumns** en una clase determinada, esa clase usará esas columnas y no las combinará con las columnas que se especifican en la clase **de presentación predeterminada** .</span><span class="sxs-lookup"><span data-stu-id="f1e60-136">If you specify the **extraColumns** attribute on a given class, then that class will use those columns and will not merge them with the columns that are specified in the **default-Display** class.</span></span> <span data-ttu-id="f1e60-137">Por lo tanto, los cambios adicionales en la clase **de presentación predeterminada** no surtirán efecto en ese objeto.</span><span class="sxs-lookup"><span data-stu-id="f1e60-137">Therefore, further changes to the **default-Display** class will have no effect on that object.</span></span>

<span data-ttu-id="f1e60-138">Para mostrar una columna personalizada para todos los tipos de contenedor que no tengan columnas personalizadas registradas, agregue un valor para la columna al atributo **Extracolumns** del objeto de **presentación predeterminada** .</span><span class="sxs-lookup"><span data-stu-id="f1e60-138">To display a custom column for all container types that do not have any custom columns registered, add a value for the column to the **extraColumns** attribute of the **default-Display** object.</span></span>

 

 




