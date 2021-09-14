---
title: Exposición de Owner-Drawn de menú
description: Exposición de Owner-Drawn de menú
ms.assetid: 93b51cbb-b7b4-4a38-ba69-d6345a269944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e79668115cedd5fb6b8c20b0d4df361d6d1d800
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160568"
---
# <a name="exposing-owner-drawn-menu-items"></a>Exposición de Owner-Drawn de menú

Los desarrolladores de aplicaciones pueden usar [**la estructura MSAAMENUINFO para**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) exponer los nombres de los elementos de menú dibujados por el propietario. Al asociar esta estructura a los datos del elemento de menú dibujado por el propietario, no es necesario exponer los elementos de menú con [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).

Al crear un menú dibujado por el propietario, defina una clase o estructura para los datos del elemento de menú dibujado por el propietario y cree instancias de esta clase para cada elemento de menú. Pase un puntero a los datos del elemento al agregar elementos al menú.

Para exponer los nombres de los elementos de menú, la estructura [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) debe ser el primer miembro de la estructura que define los datos de elementos específicos de la aplicación, como se muestra en el ejemplo siguiente:


```C++
// Application-specific owner-drawn menu info struct. Owner-drawn data 
// is a pointer to one of these.
struct MenuEntry
{
    MSAAMENUINFO m_MSAA;       // MSAA info - must be first member
    LPTSTR       m_pName;      // Displayed menu text or NULL for 
                               //   separator item 
    int          m_CmdID;      // Menu command ID 
    int          m_IconIndex;  // Index of icon in bitmap or -1 for
                               //   for separator 
};
```



La [**estructura MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) no puede ser miembro de una clase que contenga funciones virtuales. Cuando se compila el código, el primer miembro de la clase siempre es un puntero generado por el compilador a una tabla de las funciones virtuales. Para solucionar este problema, cree una estructura de datos de elemento que contenga **MSAAMENUINFO** como primer miembro. El segundo miembro es un puntero a una instancia de la clase que define los datos dibujados por el propietario. En el ejemplo siguiente se muestra esta técnica.


```C++
// Application-defined class that contains the owner-drawn data and 
//  virtual functions that operate on that data.  
class MenuEntry
{
    LPTSTR       m_pName;      // Displayed menu text or NULL for 
                               //  separator item. 
    int          m_CmdID;      // Menu command ID 
    int          m_IconIndex;  // Index of icon in bitmap or -1 for
                               //  separator item 
    virtual void m_AnimateIcon();  
    virtual void m_ChangeIconColor();
}

// Application-defined struct that contains MSAAMENUINFO as first 
//  member. Second member points to owner-drawn data. 
struct MenuInfo
{
    MSAAMENUINFO m_MSAA;       // MSAA info - must be first member
    MenuEntry *pMenuData;      // Points to the owner-drawn data 
}
```



Al agregar elementos al menú, pase un puntero a una instancia de la estructura que contiene [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) para exponer los nombres de los elementos de menú.

 

 




