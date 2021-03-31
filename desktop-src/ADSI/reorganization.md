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
# <a name="reorganization"></a>Reorganización

La organización de ventas se ha migrado a una nueva organización, "ventas y soporte técnico". Julia Bankert se ha promocionado al Vicepresidente y liderará la nueva organización. Joe Worden, el administrador de la empresa, debe trasladar las unidades organizativas de ventas a una nueva unidad organizativa, ventas y soporte técnico.


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=COM")
Set salesSupport = dom.Create("organizationalUnit", "CN=Sales and Support")
Set sales = salesSupport.MoveHere("LDAP://OU=Sales,DC=Fabrikam,DC=COM", vbNullString)
```



Con este ejemplo de código, todos los objetos de la unidad organizativa sales, incluidas las unidades organizativas, se mueven a la nueva unidad organizativa.

Ahora, Joe puede trasladar Julia a la unidad organizativa de ventas y soporte técnico.


```VB
Set usr = salesSupport.MoveHere("LDAP://CN=Julie Bankert,OU=Sales,OU=Sales and Support,DC=Fabrikam,DC=COM")
usr.Put "title", "Vice President"
usr.SetInfo
```



Tenga en cuenta que el vínculo de informe Director-directo entre Julia Bankert y Chris Gray se actualiza automáticamente mediante Active Directory.

**Para crear un informe de Active Directory**

1.  Abra Visual Basic versión 6,0 y, cuando se le pida el tipo de proyecto, seleccione **proyecto de datos**.
2.  En **proyecto de datos**, haga doble clic en **Environment1 de datos**.
3.  En la ventana **entorno de datos** , haga clic con el botón secundario en el objeto de conexión **(Connection1)** y seleccione **propiedades**.
4.  Seleccione **proveedor de OLE DB para servicios de directorio de Microsoft** y haga clic en **siguiente**.
5.  Seleccione **usar seguridad integrada de Windows NT** y haga clic en **Aceptar**. Esto crea un objeto de conexión.
6.  Vuelva a hacer clic con el botón secundario en la ventana del **entorno de datos** para seleccionar **Agregar comando**. Haga clic con el botón secundario en el objeto **Command1** y seleccione **propiedades**. Aparecerá el siguiente cuadro de diálogo **propiedades de Command1** .

    ![cuadro de diálogo Propiedades de Command1](images/adadsi3.png)

7.  Haga clic en el botón de opción **instrucción SQL** y escriba lo siguiente:

    Seleccione Name, telephoneNumber de ' LDAP://DC = Fabrikam, DC = com ', donde objectCategory = ' Person ' y objectClass = ' User '

    Se crea el objeto de **comando** . Agregue el objeto de **comando** al informe.

8.  Haga doble clic en **Data informe1** en la ventana **proyecto** .
9.  Arrastre el objeto **Command1** desde la ventana **DataEnvironment1** a la sección de **detalles** de la ventana de **Informe de datos** .
10. En **propiedades de DataReport1**, en **DataSource**, seleccione **DataEnvironment1** en el menú desplegable y seleccione **Command1** en el campo **DataMember** .
11. En la ventana proyecto, haga clic con el botón derecho en **proyecto de datos** y seleccione **propiedades de proyecto**.
12. En el cuadro de diálogo Propiedades de proyecto de **proyecto** , en **objeto de inicio**, seleccione **DataReport1** en el menú desplegable. Haz clic en **Aceptar** para guardar.
13. Compilación. Aparecerá el siguiente cuadro de diálogo **DataReport1** .

    ![cuadro de diálogo datareport1](images/adadsi4.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Combinar datos heterogéneos](joining-heterogeneous-data.md)
</dt> </dl>

 

 




