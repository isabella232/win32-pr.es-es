---
title: Usar un objeto de datos ActiveX para enlazar a proveedores ADSI
description: Como ADSI también es un proveedor de OLE DB, puede utilizar un objeto de datos ActiveX (ADO) para conectarse a los proveedores ADSI.
ms.assetid: b42d804b-f1eb-4085-88aa-015a92309ee8
ms.tgt_platform: multiple
keywords:
- ADSI (objeto de datos ActiveX)
- ADSI Data Object ADSI, usar ADO para enlazar a proveedores ADSI
- proveedores de servicios ADSI, uso del objeto de datos ActiveX para enlazar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efb64da28d5c4c2596fcf889e3b3db88b77205c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075055"
---
# <a name="using-an-activex-data-object-to-bind-to-adsi-providers"></a>Usar un objeto de datos ActiveX para enlazar a proveedores ADSI

Como ADSI también es un proveedor de OLE DB, puede utilizar un objeto de datos ActiveX (ADO) para conectarse a los proveedores ADSI. Al igual que con otros proveedores de ADO, para conectarse a un proveedor de OLE DB, debe crear un nuevo objeto de conexión y, opcionalmente, especificar las credenciales. El nombre del proveedor de OLE DB ADSI es **ADsDSOObject**.

Por ejemplo:


```VB
Dim con As New Connection 
'VBScript use: con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
con.Open "YourDescriptionHere"
```



En el ejemplo anterior, está conectado en nombre del usuario actual. Para especificar otras credenciales, use las propiedades de conexión:


```VB
con.Provider = "ADsDSOObject"
con.Properties("User ID") = "jeffsmith"
con.Properties("Password") = "guesswhat?"
con.Properties("Encrypt Password") = True
con.Open "YourDescriptionHere"
```



ADSI OLE DB define las siguientes propiedades de conexión.



| Propiedad           | Tipo de datos   | Valor predeterminado   |
|--------------------|-------------|-----------|
| "ID. de usuario"          | **UTILICEN**    | **NULL**  |
| "Password"         | **UTILICEN**    | **NULL**  |
| "Cifrar contraseña" | **BOOLEANO** | **FALSE** |
| "Marca ADSI"        | **Long**    | 0         |



 

Con OLE DB ADO, no se puede enlazar a un objeto específico. Sin embargo, puede consultar un objeto específico y obtener un conjunto de resultados. Solo los proveedores ADSI que admiten [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) se benefician de tener ADO como modelo de programación.

La propiedad marca ADSI se usa para especificar la opción de autenticación de enlace. Esta propiedad puede ser una combinación de marcas de la enumeración de enumeración de [**\_ \_ autenticación ADS**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) .

 

 




