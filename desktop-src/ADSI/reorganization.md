---
title: Reorganización
description: La organización de ventas se ha trasladado a una nueva organización \ 8212; \ 0034; Ventas y soporte técnico. \ 0034; Julia Bankert se ha promocionado como vicepresidenta y dirigirá la nueva organización.
ms.assetid: 38b05d0b-2739-43c2-aac7-7555a5bfbc91
ms.tgt_platform: multiple
keywords:
- ADSI de reorganización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368b4db1909c50242e3eda1402e46896e54785aa66739b324995b7edbdd1b007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690769"
---
# <a name="reorganization"></a>Reorganización

La organización de ventas se ha trasladado a una nueva organización: "Ventas y soporte técnico". Julia Bankert se ha promocionado como vicepresidenta y dirigirá la nueva organización. Joe Worden, administrador de empresa, debe mover la unidad organizativa Ventas a una nueva unidad organizativa, Ventas y soporte técnico.


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=COM")
Set salesSupport = dom.Create("organizationalUnit", "CN=Sales and Support")
Set sales = salesSupport.MoveHere("LDAP://OU=Sales,DC=Fabrikam,DC=COM", vbNullString)
```



Con este ejemplo de código, todos los objetos de la unidad organizativa de ventas, incluidas las unidades suba organizativas, se mueven a la nueva unidad organizativa.

Ahora, Joe puede mover a Julia a la unidad organizativa Ventas y soporte técnico.


```VB
Set usr = salesSupport.MoveHere("LDAP://CN=Julie Bankert,OU=Sales,OU=Sales and Support,DC=Fabrikam,DC=COM")
usr.Put "title", "Vice President"
usr.SetInfo
```



Tenga en cuenta que el vínculo de informe directo del administrador entre Julia Bankert y Chris Gray se actualiza automáticamente mediante Active Directory.

**Para crear un informe Active Directory datos**

1.  Abra Visual Basic versión 6.0 y, cuando se le solicite el tipo de proyecto, seleccione **Data Project**.
2.  En **Data Project**, haga doble clic en Entorno de **datos1**.
3.  En la **ventana Entorno de** datos, haga clic con el botón derecho en el objeto de conexión **(Connection1)** y seleccione **Propiedades.**
4.  Seleccione **OLE DB proveedor de servicios de directorio de Microsoft** y haga clic en **Siguiente.**
5.  Seleccione **Usar Windows seguridad integrada de NT y** haga clic en **Aceptar.** Esto crea un objeto de conexión.
6.  Haga clic con el botón derecho **en la ventana Entorno** de datos de nuevo para seleccionar Agregar **comando**. Haga clic con el botón derecho **en el objeto Command1** y seleccione **Propiedades.** Aparecerá el siguiente cuadro de diálogo Propiedades de **Command1.**

    ![cuadro de diálogo de propiedades command1](images/adadsi3.png)

7.  Haga clic **en SQL botón de opción Instrucción** y escriba lo siguiente:

    SELECT Name,telephoneNumber FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectCategory='Person' AND objectClass='user'

    Se **crea el** objeto Command. Agregue el **objeto Command** al informe.

8.  Haga doble clic **en Informe de datos1** en **Project** ventana.
9.  Arrastre el **objeto Command1** desde la **ventana DataEnvironment1** hasta la **sección Detalles** de la ventana **Informe de** datos.
10. En **Propiedades de DataReport1,** para **DataSource,** seleccione **DataEnvironment1** en el menú desplegable y seleccione **Comando1** en el **campo DataMember.**
11. En la ventana del proyecto, haga clic con el botón **derecho en Data Project** y seleccione **DataProject Properties (Propiedades del proyecto de datos).**
12. En la **ventana de diálogo DataProject - Project Propiedades,** en **Objeto** de inicio , seleccione **DataReport1** en el menú desplegable. Haz clic en **Aceptar** para guardar.
13. Compilación. Aparecerá el siguiente cuadro de diálogo **DataReport1.**

    ![datareport1 , cuadro de diálogo](images/adadsi4.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Unión de datos heterogéneos](joining-heterogeneous-data.md)
</dt> </dl>

 

 




