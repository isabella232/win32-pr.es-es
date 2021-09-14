---
description: La base de datos del producto contiene información sobre un producto. Para obtener más información sobre cómo obtener información del producto con funciones de enumeración, vea Inicializar una aplicación.
ms.assetid: 528c915c-296c-4620-8105-0b5d543e56a5
title: Obtener información de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dce842f057efb65b6d0db3ad0407a19bf08435
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074726"
---
# <a name="getting-application-information"></a>Obtener información de la aplicación

La base de datos del producto contiene información sobre un producto. Para obtener más información sobre cómo obtener información del producto con funciones de enumeración, vea [Inicializar una aplicación.](initializing-an-application.md)

**Para obtener información del producto**

1.  Compruebe que un producto está instalado llamando a la [**función MsiQueryProductState.**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)
2.  Abra la base de datos y obtenga un identificador para ella mediante una llamada a [**la función MsiOpenProduct.**](/windows/desktop/api/Msi/nf-msi-msiopenproducta)

    Si la base de datos está contenida en un paquete de instalación, llame a la [**función MsiOpenPackage.**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)

3.  Use el identificador abierto para obtener las propiedades del producto con la función [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) y para obtener información de características descriptiva con la [**función MsiGetFeatureInfo.**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)

    Si desea obtener información del producto mediante el código de producto, en lugar de usar el identificador de base de datos abierto, llame a la función [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) en lugar de [**a MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya).

4.  Cierre un identificador de instalación abierto llamando a [**la función MsiCloseHandle.**](/windows/desktop/api/Msi/nf-msi-msiclosehandle)

    La [**función MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) es una función de diagnóstico y no debe usarse para cerrar los identificadores que sabe que están abiertos. Es aceptable llamar a la función **MsiCloseAllHandles** cuando la aplicación se cierra para asegurarse de que se han cerrado todos los identificadores.

 

 



