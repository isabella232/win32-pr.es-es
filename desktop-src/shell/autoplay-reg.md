---
description: Hay muchas situaciones en las que la ejecución automática puede tener que deshabilitarse temporal o persistentemente.
ms.assetid: 5e65a3d8-04b9-46ba-b4e5-a976e1923bfd
title: Habilitar y deshabilitar la ejecución automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567f50db75cd129346e193e66ba0ae5f74fa955
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363175"
---
# <a name="enabling-and-disabling-autorun"></a>Habilitar y deshabilitar la ejecución automática

Hay muchas situaciones en las que la ejecución automática puede tener que deshabilitarse temporal o persistentemente. Por ejemplo, La ejecución automática puede interferir con el funcionamiento de una aplicación en ejecución y debe deshabilitarse mientras dure. El sistema proporciona varias maneras de deshabilitar AutoRun.

-   [Suprimir la ejecución automática mediante programación](#suppressing-autorun-programmatically)
-   [Uso del Registro para deshabilitar AutoRun](#using-the-registry-to-disable-autorun)
-   [AutoRun for Other Types of Storage Media](#autorun-for-other-types-of-storage-media)

## <a name="suppressing-autorun-programmatically"></a>Suprimir la ejecución automática mediante programación

Hay una variedad de situaciones en las que la ejecución automática puede tener que suprimirse mediante programación. Dos ejemplos son:

-   La aplicación tiene un programa de instalación que requiere que el usuario inserte otro disco que pueda contener un archivo Autorun.inf.
-   Durante el funcionamiento de la aplicación, es posible que el usuario tenga que insertar otro disco que pueda contener un archivo Autorun.inf.

En cualquier caso, normalmente no querrá iniciar otra aplicación mientras el original está en curso.

Los usuarios pueden suprimir manualmente AutoRun manteniendo presionada la tecla MAYÚS al insertar el CD-ROM. Sin embargo, normalmente es preferible controlar esta operación mediante programación en lugar de depender del usuario.

Con los sistemas que tienen la versión [4.70](versions.md) de Shell y versiones posteriores, Windows envía un mensaje "QueryCancelAutoPlay" a la ventana de primer plano. La aplicación puede responder a este mensaje para suprimir AutoRun. Este enfoque lo usan utilidades del sistema, como el [cuadro de](../dlgbox/open-and-save-as-dialog-boxes.md) diálogo Abrir común para deshabilitar La ejecución automática.

Los fragmentos de código siguientes muestran cómo configurar y controlar este mensaje. La aplicación debe ejecutarse en la ventana de primer plano. En primer lugar, registre "QueryCancelAutoPlay" como Windows mensaje:


```C++
uMessage = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
```



La ventana de la aplicación debe estar en primer plano para recibir este mensaje. El controlador de mensajes debe devolver **TRUE** para cancelar AutoRun y **FALSE** para habilitarlo. En el fragmento de código siguiente se muestra cómo usar este mensaje para deshabilitar AutoRun.


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



Si la aplicación usa un cuadro de diálogo y necesita responder a un mensaje "QueryCancelAutoPlay", no puede devolver **simplemente TRUE** o **FALSE.** En su lugar, [**llame a SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) con *nIndex* establecido en **DWL \_ MSGRESULT**. Establezca el *parámetro dwNewLong* en **TRUE para** cancelar AutoRun y **FALSE** para habilitarlo. Por ejemplo, el siguiente procedimiento de cuadro de diálogo de ejemplo cancela AutoRun cuando recibe un mensaje "QueryCancelAutoPlay".


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



## <a name="using-the-registry-to-disable-autorun"></a>Uso del Registro para deshabilitar AutoRun

Hay dos valores del Registro que se pueden usar para deshabilitar de forma persistente AutoRun: NoDriveAutoRun y NoDriveTypeAutoRun. El primer valor deshabilita AutoRun para las letras de unidad especificadas y el segundo deshabilita AutoRun para una clase de unidades. Si alguno de estos valores se establece para deshabilitar AutoRun para un dispositivo determinado, se deshabilitará. Consulte el Knowledge Base artículo Deshabilitación de la funcionalidad de ejecución [automática en Windows](https://support.microsoft.com/kb/967715) para obtener más información sobre cómo deshabilitar la funcionalidad de ejecución automática. En este artículo se enumeran las distintas actualizaciones que debe haber instalado para deshabilitar correctamente la funcionalidad de ejecución automática.

> [!Note]  
> Los valores NoDriveAutoRun y NoDriveTypeAutoRun solo los deben modificar los administradores del sistema para cambiar el valor de todo el sistema con fines administrativos o de prueba. Las aplicaciones no deben modificar estos valores, ya que no hay ninguna manera de restaurarlos de forma confiable a sus valores originales.

 

El valor NoDriveAutoRun deshabilita AutoRun para las letras de unidad especificadas. Es un valor de \_ datos REG DWORD, que se encuentra en la clave siguiente:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

El primer bit del valor corresponde a la unidad A:, la segunda a B:, y así sucesivamente. Para deshabilitar AutoRun para una o varias letras de unidad, establezca los bits correspondientes. Por ejemplo, para deshabilitar las unidades A: y C:, establezca NoDriveAutoRun en `0x00000005` .

El valor NoDriveTypeAutoRun deshabilita AutoRun para una clase de unidades. Es un valor de datos REG DWORD o REG BINARY de \_ 4 \_ bytes, que se encuentra en la misma clave.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

Al establecer los bits del primer byte de este valor, se pueden excluir unidades diferentes para que no funcionen con AutoRun.

La tabla siguiente proporciona los bits y las constantes de máscara de bits, que se pueden establecer en el primer byte de NoDriveTypeAutoRun para deshabilitar AutoRun para un tipo de unidad determinado. Debe reiniciar el explorador Windows antes de que los cambios sumen efecto.



| Número de bits | Constante de máscara de bits      | Descripción                                             |
|------------|-----------------------|---------------------------------------------------------|
| 0x04       | **UNIDAD \_ EXTRAÍBLE** | El disco se puede quitar de la unidad (por ejemplo, un disquete). |
| 0x08       | **UNIDAD \_ FIJA**      | No se puede quitar el disco de la unidad (un disco duro).        |
| 0x10       | **UNIDAD \_ REMOTA**     | Unidad de red.                                          |
| 0x20       | **UNIDAD \_ CDROM**      | Unidad de CD-ROM.                                           |
| 0x40       | **UNIDAD \_ RAMDISK**    | Disco RAM.                                               |



 

## <a name="autorun-for-other-types-of-storage-media"></a>AutoRun for Other Types of Storage Media

La ejecución automática está pensada principalmente para la distribución pública de aplicaciones en CD-ROM y DVD-ROM, y no se recomienda su uso para otros medios de almacenamiento. Sin embargo, a menudo resulta útil habilitar AutoRun en otros tipos de medios de almacenamiento extraíbles. Esta característica se usa normalmente para simplificar la depuración de archivos AutoRun.inf. La ejecución automática solo funciona en dispositivos de almacenamiento extraíbles cuando se cumplen los siguientes criterios:

-   El dispositivo debe tener controladores compatibles con AutoRun. Para que sea compatible con AutoRun, un controlador debe notificar al sistema que se ha insertado un disco mediante el envío de [**un mensaje DE WM \_ DEVICECHANGE.**](../devio/wm-devicechange.md)
-   El directorio raíz del medio insertado debe contener un archivo Autorun.inf.
-   El dispositivo no debe tener la ejecución automática deshabilitada a través del [registro](#using-the-registry-to-disable-autorun).
-   La aplicación en primer plano no [ha suprimido AutoRun.](#suppressing-autorun-programmatically)

> [!Note]  
> Esta característica no debe usarse para distribuir aplicaciones en medios extraíbles. Dado que la implementación de AutoRun en medios extraíbles proporciona una manera fácil de propagar virus informáticos, los usuarios deben ser sospechosos de cualquier disquete distribuido públicamente que contenga un archivo Autorun.inf.

 

Normalmente, AutoRun se inicia automáticamente, pero también se puede iniciar manualmente. Si el dispositivo cumple los criterios mencionados anteriormente, el menú contextual de la letra de unidad incluirá un **comando De reproducción** automática. Para ejecutar AutoRun manualmente, haga clic con el botón derecho en el icono de unidad y seleccione **Reproducción** automática en el menú contextual o haga doble clic en el icono de unidad. Si los controladores no son compatibles con AutoRun, el menú contextual no tendrá un elemento **Reproducción** automática y No se puede iniciar AutoRun.

Los controladores compatibles con AutoRun se proporcionan con algunas unidades de disco extraíbles, así como otros tipos de medios extraíbles, como tarjetas CompactFlash. AutoRun también funciona con unidades de red que están asignadas a una letra de unidad con Windows Explorer o montadas con [el Microsoft Management Console (MMC).](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) Al igual que con el hardware montado, una unidad de red montada debe tener un archivo Autorun.inf en su directorio raíz y no debe deshabilitarse a través del [Registro](#using-the-registry-to-disable-autorun).

 

 
