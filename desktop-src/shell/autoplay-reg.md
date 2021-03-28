---
description: Hay muchas situaciones en las que la ejecución automática puede tener que estar deshabilitada de forma temporal o permanente.
ms.assetid: 5e65a3d8-04b9-46ba-b4e5-a976e1923bfd
title: Habilitar y deshabilitar la ejecución automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567f50db75cd129346e193e66ba0ae5f74fa955
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423723"
---
# <a name="enabling-and-disabling-autorun"></a>Habilitar y deshabilitar la ejecución automática

Hay muchas situaciones en las que la ejecución automática puede tener que estar deshabilitada de forma temporal o permanente. Por ejemplo, la ejecución automática podría interferir con el funcionamiento de una aplicación en ejecución y debe deshabilitarse mientras dure. El sistema proporciona varias formas de deshabilitar la ejecución automática.

-   [Suprimir la ejecución automática mediante programación](#suppressing-autorun-programmatically)
-   [Usar el registro para deshabilitar la ejecución automática](#using-the-registry-to-disable-autorun)
-   [Ejecución automática para otros tipos de medios de almacenamiento](#autorun-for-other-types-of-storage-media)

## <a name="suppressing-autorun-programmatically"></a>Suprimir la ejecución automática mediante programación

Hay varias situaciones en las que es posible que sea necesario suprimir la ejecución automática mediante programación. Dos ejemplos son:

-   La aplicación tiene un programa de instalación que requiere que el usuario inserte otro disco que puede contener un archivo Autorun. inf.
-   Durante el funcionamiento de la aplicación, es posible que el usuario tenga que insertar otro disco que pueda contener un archivo Autorun. inf.

En cualquier caso, normalmente no querrá iniciar otra aplicación mientras el original está en curso.

Los usuarios pueden suprimir manualmente la ejecución automática manteniendo presionada la tecla Mayús al insertar el CD-ROM. Sin embargo, suele ser preferible controlar esta operación mediante programación en lugar de depender del usuario.

Con los sistemas que tienen la versión de Shell [4,70](versions.md) y versiones posteriores, Windows envía un mensaje "QueryCancelAutoPlay" a la ventana de primer plano. La aplicación puede responder a este mensaje para suprimir la ejecución automática. Las utilidades del sistema utilizan este enfoque, como el cuadro de diálogo [abrir](../dlgbox/open-and-save-as-dialog-boxes.md) común para deshabilitar la ejecución automática.

Los fragmentos de código siguientes muestran cómo configurar y controlar este mensaje. La aplicación debe ejecutarse en la ventana de primer plano. En primer lugar, registre "QueryCancelAutoPlay" como mensaje de Windows:


```C++
uMessage = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
```



La ventana de la aplicación debe estar en primer plano para recibir este mensaje. El controlador de mensajes debe devolver **true** para cancelar la ejecución automática y **false** para habilitarla. En el fragmento de código siguiente se muestra cómo utilizar este mensaje para deshabilitar la ejecución automática.


```C++
UINT g_uQueryCancelAutoPlay = 0;

LRESULT WndProc(HWND hwnd, UINT uMsg,  WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ... 
    default: 
        if (!g_uQueryCancelAutoPlay)
        { 
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg && uMsg == g_uQueryCancelAutoPlay)
        { 
            return TRUE;       // Cancel AutoRun
        }
    }
}
```



Si la aplicación usa un cuadro de diálogo y necesita responder a un mensaje "QueryCancelAutoPlay", no puede devolver simplemente **true** o **false**. En su lugar, llame a [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) con *NIndex* establecido en **DWL \_ MSGRESULT**. Establezca el parámetro *dwNewLong* en **true** para cancelar la ejecución automática y **false** para habilitarla. Por ejemplo, el procedimiento de cuadro de diálogo de ejemplo siguiente cancela la ejecución automática cuando recibe un mensaje "QueryCancelAutoPlay".


```C++
UINT g_uQueryCancelAutoPlay = 0;

BOOL DialogProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ...
    default: 
        if (!g_uQueryCancelAutoPlay)
        {
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg == g_uQueryCancelAutoPlay) 
        {
            SetWindowLong(hDlg, DWL_MSGRESULT, TRUE);          
            return 1;               
        }
    } 
```



## <a name="using-the-registry-to-disable-autorun"></a>Usar el registro para deshabilitar la ejecución automática

Hay dos valores de registro que se pueden usar para deshabilitar de forma persistente la ejecución automática: NoDriveAutoRun y NoDriveTypeAutoRun. El primer valor deshabilita la ejecución automática de las letras de unidad especificadas y la segunda deshabilita la ejecución automática para una clase de unidades. Si alguno de estos valores se establece para deshabilitar la ejecución automática de un dispositivo determinado, se deshabilitará. Vea el artículo de Knowledge base [cómo deshabilitar la funcionalidad de ejecución automática en Windows](https://support.microsoft.com/kb/967715) para obtener más información sobre cómo deshabilitar la funcionalidad de ejecución automática. En este artículo se enumeran las diferentes actualizaciones que debe tener instaladas para deshabilitar correctamente la funcionalidad de ejecución automática.

> [!Note]  
> Los valores de NoDriveAutoRun y NoDriveTypeAutoRun solo deben ser modificados por los administradores del sistema para cambiar el valor de todo el sistema con fines de prueba o administrativos. Las aplicaciones no deben modificar estos valores, ya que no hay ninguna manera de restaurarlos de forma confiable a sus valores originales.

 

El valor NoDriveAutoRun deshabilita la ejecución automática de las letras de unidad especificadas. Es un valor de \_ datos de REG DWORD, que se encuentra en la clave siguiente:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

El primer bit del valor corresponde a la unidad a:, la segunda a B:, etc. Para deshabilitar la ejecución automática de una o varias letras de unidad, establezca los bits correspondientes. Por ejemplo, para deshabilitar las unidades A: y C:, establezca NoDriveAutoRun en `0x00000005` .

El valor NoDriveTypeAutoRun deshabilita AutoRun para una clase de unidades. Es un valor de \_ datos binario de REG DWORD o de 4 bytes \_ , que se encuentra en la misma clave.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

Al establecer los bits del primer byte de este valor, se pueden excluir las diferentes unidades de trabajo con la ejecución automática.

En la tabla siguiente se proporcionan las constantes de bits y máscara de bits que se pueden establecer en el primer byte de NoDriveTypeAutoRun para deshabilitar la ejecución automática de un tipo de unidad determinado. Debe reiniciar el explorador de Windows para que los cambios surtan efecto.



| Número de bits | Constante de máscara de máscara      | Descripción                                             |
|------------|-----------------------|---------------------------------------------------------|
| 0x04       | **UNIDAD que se \_ va a cambiar** | El disco se puede quitar de la unidad (por ejemplo, un disquete). |
| 0x08       | **UNIDAD \_ fija**      | No se puede quitar el disco de la unidad (un disco duro).        |
| 0x10       | **UNIDAD \_ remota**     | Unidad de red.                                          |
| 0x20       | **UNIDAD \_ CDROM**      | Unidad de CD-ROM.                                           |
| 0x40       | **DISCO \_ ramdisk**    | Disco RAM.                                               |



 

## <a name="autorun-for-other-types-of-storage-media"></a>Ejecución automática para otros tipos de medios de almacenamiento

La ejecución automática está pensada principalmente para la distribución pública de aplicaciones en CD-ROM y DVD-ROM, y no se recomienda su uso en otros medios de almacenamiento. Sin embargo, a menudo resulta útil habilitar la ejecución automática en otros tipos de medios de almacenamiento extraíbles. Esta característica se usa normalmente para simplificar la depuración de archivos AutoRun. inf. La ejecución automática solo funciona en dispositivos de almacenamiento extraíbles cuando se cumplen los siguientes criterios:

-   El dispositivo debe tener controladores compatibles con AutoRun. Para que sea compatible con la ejecución automática, un controlador debe notificar al sistema que se ha insertado un disco mediante el envío de un mensaje de [**\_ DEVICECHANGE de WM**](../devio/wm-devicechange.md) .
-   El directorio raíz del medio insertado debe contener un archivo Autorun. inf.
-   El dispositivo no debe tener la ejecución automática deshabilitada a través del [registro](#using-the-registry-to-disable-autorun).
-   La aplicación en primer plano no ha [suprimido](#suppressing-autorun-programmatically) la ejecución automática.

> [!Note]  
> Esta característica no debe usarse para distribuir aplicaciones en medios extraíbles. Dado que la implementación de la ejecución automática en medios extraíbles proporciona una manera sencilla de propagar los virus informáticos, los usuarios deben ser sospechosos de cualquier disquete distribuido públicamente que contenga un archivo Autorun. inf.

 

Normalmente, la ejecución automática se inicia automáticamente, pero también se puede iniciar manualmente. Si el dispositivo cumple los criterios indicados anteriormente, el menú contextual de la letra de la unidad incluirá un comando de **reproducción automática** . Para ejecutar la ejecución automática manualmente, haga clic con el botón derecho en el icono de la unidad y seleccione **reproducción automática** en el menú contextual o haga doble clic en el icono de la unidad. Si los controladores no son compatibles con la ejecución automática, el menú contextual no tendrá un elemento **reproducción automática** y no se podrá iniciar la ejecución automática.

Los controladores compatibles con AutoRun se proporcionan con algunas unidades de disco extraíbles, así como otros tipos de medios extraíbles, como tarjetas CompactFlash. La ejecución automática también funciona con las unidades de red asignadas a una letra de unidad con el explorador de Windows o montadas con [Microsoft Management Console (MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page). Al igual que con el hardware montado, una unidad de red montada debe tener un archivo Autorun. inf en el directorio raíz y no debe deshabilitarse a través del [registro](#using-the-registry-to-disable-autorun).

 

 
