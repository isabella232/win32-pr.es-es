---
description: Si decide implementar el borrado en la aplicación que no sea mediante el objeto InkOverlay, puede hacerlo mediante uno de los dos métodos siguientes.
ms.assetid: c05c7dbf-c3e0-42a7-a97e-bb9d9764209d
title: Borrado mediante el lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9e71828e826f2d57dd21e57934e12c8de0be03
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247844"
---
# <a name="erasing-by-using-the-pen"></a>Borrado mediante el lápiz

Si decide implementar el borrado en la aplicación que no sea mediante el objeto [**InkOverlay,**](inkoverlay-class.md) puede hacerlo mediante uno de los dos métodos siguientes.

## <a name="using-the-tip-of-the-pen"></a>Usar la sugerencia del lápiz

La sugerencia del lápiz de tableta se usa generalmente para escribir a mano y dibujar. sin embargo, la sugerencia también se puede usar para borrar la entrada de lápiz. Para ello, la aplicación debe tener un modo de borrado que los usuarios puedan emplear. En este modo, use las pruebas de posición para determinar qué entrada manuscrita se mueve el cursor. Puede establecer el modo de borrado para eliminar solo la entrada de lápiz que pasa el cursor o los trazos enteros que intersecan con la ruta de acceso del cursor, en función de las consideraciones de diseño o funcionales.

Para obtener un ejemplo de cómo usar un modo de borrado para borrar la entrada de lápiz, vea El ejemplo [de borrado de lápiz](ink-erasing-sample.md).

## <a name="using-the-top-of-the-pen"></a>Uso de la parte superior del lápiz

Para implementar el borrado con la parte superior del lápiz de tableta, la aplicación debe buscar un cambio en el cursor. Para buscar el cursor invertido, escuche el evento [**CursorInRange**](inkoverlay-cursorinrange.md) para determinar cuándo se encuentra el cursor en el contexto de la aplicación. Cuando el cursor esté dentro del intervalo, busque la [**propiedad Inverted**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) en el [**objeto Cursor.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) Si la **propiedad Inverted** es **true,** realice pruebas de impacto para determinar qué entrada manuscrita se mueve el cursor. Borre la entrada de lápiz o los trazos que intersecan con la ruta de acceso del cursor, en función de las consideraciones de diseño o funcionales.

Para obtener un ejemplo de cómo usar la parte superior del lápiz para borrar la entrada de lápiz, vea El ejemplo [de borrado de lápiz](ink-erasing-sample.md).

### <a name="determining-if-erasing-with-the-top-of-the-pen-is-enabled"></a>Determinar si el borrado con la parte superior del lápiz está habilitado

Los usuarios pueden usar la parte superior del lápiz para borrar la entrada de lápiz en aplicaciones diseñadas para Tablet PC, si su hardware determinado lo permite. Se puede acceder a esta funcionalidad mediante una casilla del cuadro de grupo Botones de lápiz de la pestaña Opciones del lápiz del cuadro de diálogo Del panel de control tablet Configuración Pen. Para detectar si el usuario ha habilitado el borrado en la parte superior del lápiz, compruebe la siguiente subclave del Registro:

`HKEY_CURRENT_USER\SOFTWARE\Microsoft\WISP\PEN\SysEventParameters`

La `EraseEnable` entrada de esta subclave es de tipo REG **\_ DWORD**. El valor de esta entrada es 1 para habilitado o 0 para deshabilitado. Otros valores se reservan para un uso futuro.

Si la aplicación permite usar la parte superior del lápiz para borrar, debe comprobar y almacenar en caché el valor de la entrada EraseEnable cuando:

-   Se inicia la aplicación.
-   Cada vez que la aplicación recibe el foco después de perder el foco.

Use este valor almacenado en caché para modificar el comportamiento de la aplicación correctamente.

En el siguiente ejemplo de C \# se define un método que comprueba el valor de la entrada de la `GetEraseEnabled` `EraseEnable` `SysEventParameters` subclave. El método devuelve TRUE si el valor de la entrada es 1; devuelve FALSE si el valor de la entrada es 0; o inicia una excepción InvalidOperationException si el valor de la entrada es distinto de `GetEraseEnabled` 1 o  0.  [](/dotnet/api/system.invalidoperationexception) El `GetEraseEnabled` método devuelve el valor esperado de **TRUE** si la subclave o la entrada no están presentes.


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



 

 
