---
description: La base de datos del producto contiene información acerca de un producto. Para obtener más información sobre cómo obtener información de productos con las funciones de enumeración, consulte inicializar una aplicación.
ms.assetid: 528c915c-296c-4620-8105-0b5d543e56a5
title: Obtención de información de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dce842f057efb65b6d0db3ad0407a19bf08435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001483"
---
# <a name="getting-application-information"></a>Obtención de información de la aplicación

La base de datos del producto contiene información acerca de un producto. Para obtener más información sobre cómo obtener información de productos con las funciones de enumeración, consulte [inicializar una aplicación](initializing-an-application.md).

**Para obtener información del producto**

1.  Compruebe que un producto está instalado mediante una llamada a la función [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) .
2.  Abra la base de datos y obtenga un identificador llamando a la función [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) .

    Si la base de datos se encuentra en un paquete de instalación, llame a la función [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) .

3.  Use el identificador Open para obtener las propiedades de producto con la función [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) y para obtener información de características descriptiva con la función [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) .

    Si desea obtener información del producto con el código de producto, en lugar de usar el identificador de base de datos abierto, llame a la función [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) en lugar de a [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya).

4.  Cierre un identificador de instalación abierto llamando a la función [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) .

    La función [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) es una función de diagnóstico y no debe usarse para cerrar los identificadores que sabe que están abiertos. Es aceptable llamar a la función **MsiCloseAllHandles** cuando la aplicación se cierra para asegurarse de que se han cerrado todos los identificadores.

 

 



