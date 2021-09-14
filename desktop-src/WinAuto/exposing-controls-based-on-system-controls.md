---
title: Exponer controles basados en controles del sistema
description: Exponer controles basados en controles del sistema
ms.assetid: 9291b79e-3ed0-4f3c-a610-38215d84f5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2fe31eae8c2283c020de93b0c1f3350bd0f417
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160570"
---
# <a name="exposing-controls-based-on-system-controls"></a>Exponer controles basados en controles del sistema

Considere la posibilidad de usar algún tipo de anotación dinámica (Directa, Asignación de valores o Servidor) antes de intentar la técnica descrita en esta sección. Para más información, consulte [API de anotación dinámica.](dynamic-annotation-api.md)

En la mayoría de los Microsoft Active Accessibility muestra información sobre los controles superclases o subclases. Las superclases y las subclases permiten a un desarrollador de aplicaciones crear un control personalizado con la funcionalidad básica de un control del sistema e incluir mejoras proporcionadas por la aplicación. Un control superclase tiene un nombre de clase de ventana diferente al control del sistema en el que se basa. Un control con subclases tiene el mismo nombre de clase de ventana. Para obtener más información sobre las superclases y las subclases, consulte la documentación Windows Software Development Kit (SDK).

Dado Microsoft Active Accessibility información sobre los controles proporcionados por el sistema, Microsoft Active Accessibility expone el control modificado a menos que un control con superclases o subclases sea significativamente diferente del control base. Para determinar si el control modificado es accesible, los desarrolladores de aplicaciones deben usar utilidades como [Inspect](inspect-objects.md) y [Accessible Event Watcher](accessible-event-watcher.md) para comparar el comportamiento del control modificado con el control base.

Si después de usar estas utilidades determina que el control modificado no es accesible, debe tratar el control como cualquier otro control personalizado. El control debe desencadenar eventos y el procedimiento de ventana de la aplicación debe responder al mensaje [**\_ GETOBJECT**](wm-getobject.md)de WM al proporcionar una [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que las aplicaciones cliente usan para obtener información sobre el control.

## <a name="createstdaccessibleproxy-and-createstdaccessibleobject"></a>CreateStdAccessibleProxy y CreateStdAccessibleObject

Si todas o la mayoría de las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del control modificado son las mismas que el control base, use [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) o [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) para simplificar la implementación de la interfaz **IAccessible** del control.

> [!Note]  
> Al crear superclases o crear subclases de un control accesible, tenga en cuenta que el objeto recuperado por la función [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) puede implementar algo más que la [**interfaz IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Puede incluir otras interfaces como [IEnumVARIANT.](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) Es posible que tenga que ajustar estas interfaces adicionales para conservar la compatibilidad de accesibilidad proporcionada por la aplicación original del control.

 

Las [**funciones CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) y [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) recuperan un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el control del sistema especificado. La diferencia en estas funciones es que **CreateStdAccessibleObject** usa el nombre de clase de ventana obtenido de su *parámetro hwnd,* mientras que **CreateStdAccessibleProxy** usa el nombre de clase de ventana especificado en su *parámetro szClassName.* Por lo tanto, si decide usar estas funciones, use **CreateStdAccessibleProxy** para exponer información sobre los controles superclases y cualquiera de ellas con controles con subclases.

Después de obtener un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) al control del sistema, use el puntero en la implementación de la **interfaz IAccessible** para el control modificado. Si una propiedad o método para el control modificado es el mismo que el control base, use el puntero **IAccessible** para devolver la información proporcionada por el control base. Si una propiedad del control modificado es diferente del control base, invalide la propiedad del control base.

En el ejemplo siguiente, **CAccCustomButton** es la clase definida por la aplicación derivada de [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) La variable miembro **m \_ pAccDefaultButton** es un puntero a una interfaz **IAccessible** que se recuperó de [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) durante el procedimiento de inicialización del control. En este ejemplo, la propiedad **Role** del control personalizado es la misma que la propiedad **Role** del control del sistema, por lo que se devuelve la propiedad **Role** del control base. Sin embargo, **la propiedad Description** es diferente de la del control base, por lo que esta propiedad se invalida.


```C++
HRESULT CAccCustomButton::Initialize( HWND hWnd, HINSTANCE hInst )
{
.
.
.
    hr = CreateStdAccessibleObject( m_hWnd, 
                                    OBJID_CLIENT, 
                                    IID_IAccessible, 
                                    (void **) &m__pAccDefaultButton );
.
.
.
}

STDMETHODIMP CAccCustomButton::get_accRole( VARIANT varID )
{
    return m_pAccDefaultButton->get_accRole(varID);
}


STDMETHODIMP CAccCustomButton::get_accDescription( VARIANT varChild,
                                                   BSTR* pszDesc )
{
    TCHAR   szString[256];
    OLECHAR wszString[256];

    LoadString( m_hInst, ID_DESCRIPTION, szString, 256 );
    MultiByteToWideChar( CP_ACP, 0, szString, -1, wszString, 256 );
   *pszDesc = SysAllocString( wszString );
   if ( !pszDesc )
       return S_OK;
   else
       return E_OUTOFMEMORY;
}
```



Para obtener más información sobre las propiedades y métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de los controles del sistema, vea Apéndice A: Referencia de elementos Interfaz de usuario [admitidos.](appendix-a--supported-user-interface-elements-reference.md)

 

 