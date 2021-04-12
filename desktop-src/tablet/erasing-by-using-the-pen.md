---
description: Si decide implementar el borrado en la aplicación que no sea mediante el objeto InkOverlay, puede hacerlo con uno de los dos métodos siguientes.
ms.assetid: c05c7dbf-c3e0-42a7-a97e-bb9d9764209d
title: Borrar con el lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9e71828e826f2d57dd21e57934e12c8de0be03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423788"
---
# <a name="erasing-by-using-the-pen"></a>Borrar con el lápiz

Si decide implementar el borrado en la aplicación que no sea mediante el objeto [**InkOverlay**](inkoverlay-class.md) , puede hacerlo con uno de los dos métodos siguientes.

## <a name="using-the-tip-of-the-pen"></a>Usar la punta del lápiz

La sugerencia del lápiz de Tablet PC se utiliza generalmente para la escritura a mano y para el dibujo. sin embargo, la sugerencia también puede usarse para borrar la entrada de lápiz. Para ello, la aplicación debe tener un modo de borrado que los usuarios puedan emplear. En este modo, use la prueba de posicionamiento para determinar en qué entrada de lápiz se mueve el cursor. Puede establecer el modo de borrado para eliminar solo la tinta que el cursor pasa sobre o trazos completos que forman una intersección con la ruta de acceso del cursor, en función de las consideraciones de diseño o funcionales.

Para obtener un ejemplo de cómo usar un modo de borrado para borrar la entrada manuscrita, vea el [ejemplo de borrado de tinta](ink-erasing-sample.md).

## <a name="using-the-top-of-the-pen"></a>Usar la parte superior del lápiz

Para implementar el borrado con la parte superior del lápiz de Tablet PC, la aplicación debe buscar un cambio en el cursor. Para buscar el cursor invertido, escuche el evento [**CursorInRange**](inkoverlay-cursorinrange.md) para determinar si el cursor está en el contexto de la aplicación. Cuando el cursor esté en el intervalo, busque la propiedad [**invertida**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) en el objeto [**cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) . Si la propiedad **invertida** es **true**, realice la prueba de posicionamiento para determinar en qué entrada de lápiz se está moviendo el cursor. Borre la tinta o los trazos que forman una intersección con la ruta de acceso del cursor, en función de las consideraciones de diseño o funcionales.

Para obtener un ejemplo de cómo usar la parte superior del lápiz para borrar la entrada manuscrita, vea el [ejemplo de borrado de tinta](ink-erasing-sample.md).

### <a name="determining-if-erasing-with-the-top-of-the-pen-is-enabled"></a>Determinar si está habilitado el borrado con la parte superior del lápiz

Los usuarios pueden usar la parte superior del lápiz para borrar la entrada manuscrita en aplicaciones diseñadas para Tablet PC, si su hardware determinado lo permite. Se tiene acceso a esta funcionalidad mediante una casilla en el cuadro de grupo botones del lápiz de la pestaña Opciones de lápiz del cuadro de diálogo panel de control de configuración de Tablet PC y lápiz. Para detectar si el usuario ha habilitado el borrado de la parte superior del lápiz, Compruebe la siguiente subclave del registro:

`HKEY_CURRENT_USER\SOFTWARE\Microsoft\WISP\PEN\SysEventParameters`

La `EraseEnable` entrada de esta subclave es de tipo **reg \_ DWORD**. El valor de esta entrada es 1 para habilitado, o 0 para deshabilitado. Otros valores se reservan para un uso futuro.

Si la aplicación permite usar la parte superior del lápiz para borrar, debe comprobar y almacenar en caché el valor de la entrada EraseEnable cuando:

-   Se inicia la aplicación.
-   Cada vez que la aplicación recibe el foco después de perder el foco.

Use este valor almacenado en caché para modificar el comportamiento de la aplicación de forma adecuada.

En el siguiente \# ejemplo de C se define un `GetEraseEnabled` método que comprueba el valor de la `EraseEnable` entrada de la `SysEventParameters` subclave. El `GetEraseEnabled` método devuelve **true** si el valor de la entrada es 1; devuelve **false** si el valor de la entrada es 0; o produce una excepción [InvalidOperationException](/dotnet/api/system.invalidoperationexception) si el valor de la entrada es distinto de 1 o 0. El `GetEraseEnabled` método devuelve el valor esperado de **true** si la subclave o la entrada no está presente.


```C++
private bool GetEraseEnabled()
{
    // 0 is disabled, 1 is enabled. The default is enabled
    const int Enabled = 1;
    const int Disabled = 0;
    const int DefaultValue = Enabled;

    // Constants for the registry subkey and the entry
    const string Subkey =
                @"SOFTWARE\Microsoft\WISP\PEN\SysEventParameters";
    const string KeyEntry = "EraseEnable";

    // Open the registry subkey.
    Microsoft.Win32.RegistryKey regKey =
        Microsoft.Win32.Registry.CurrentUser.OpenSubKey(Subkey);

    // Retrieve the value of the EraseEnable subkey entry. If either
    // the subkey or the entry does not exist, use the default value.
    object keyValue = (null == regKey) ? DefaultValue :
        regKey.GetValue(KeyEntry,DefaultValue);

    switch((int)keyValue)
    {
        case Enabled:
            // Return true if erasing on pen inversion is enabled. 
            return true;
        case Disabled:
            // Return false if erasing on pen inversion is disabled. 
            return false;
        default:
            // Otherwise, throw an exception. Do not assume this is
            // a Boolean value. Enabled and Disabled are the values
            // defined for this entry at this time. Other values are
            // reserved for future use.
            throw new InvalidOperationException(
                "Unexpected registry subkey value.");
    }
}
```



 

 
