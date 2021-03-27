---
description: En este tema se proporciona información sobre las consideraciones de seguridad relacionadas con el shell de Windows.
ms.assetid: eca31652-2659-456d-b082-c84d6fd39094
title: 'Consideraciones de seguridad: Shell de Microsoft Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b11a965a36a403b57a3e5229fc758a4ce37252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810934"
---
# <a name="security-considerations-microsoft-windows-shell"></a>Consideraciones de seguridad: Shell de Microsoft Windows

En este tema se proporciona información sobre las consideraciones de seguridad relacionadas con el shell de Windows. En este documento no se puede proporcionar todo lo que necesita saber acerca de los problemas de seguridad, en su lugar, usarlo como punto de partida y referencia para este área de tecnología específica.

El shell controla varios aspectos importantes del sistema, incluidos los que presentan posibles riesgos de seguridad si no se controlan correctamente. En este tema se describen algunos de los problemas más comunes y cómo abordarlos en las aplicaciones. Recuerde que la seguridad no se limita a los ataques basados en Internet. En los sistemas compartidos, incluidos los sistemas a los que se puede tener acceso a través de Terminal Services, también debe asegurarse de que los usuarios no pueden hacer nada que puedan dañar a otros usuarios que comparten el sistema.

-   [Instalación correcta de la aplicación](#installing-your-application-properly)
-   [Shlwapi](#shlwapi)
-   [Autocompletar](#autocomplete)
-   [ShellExecute, ShellExecuteEx y funciones relacionadas](#shellexecute-shellexecuteex-and-related-functions)
-   [Mover y copiar archivos](#moving-and-copying-files)
-   [Escribir extensiones de espacio de nombres seguras](#writing-secure-namespace-extensions)
-   [alertas de seguridad](#security-alerts)
-   [Temas relacionados](#related-topics)

## <a name="installing-your-application-properly"></a>Instalación correcta de la aplicación

La mayoría de los posibles problemas de seguridad de Shell se pueden mitigar si se instala correctamente la aplicación.

-   Instale la aplicación en la carpeta archivos de programa. 

    | Sistema operativo                             | Location                                                                                                                                                                                                                                   |
    |----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Windows XP, Windows Server 2003 y versiones anteriores | \_archivos de programa CSIDL \_                                                                                                                                                                                                                      |
    | Windows Vista y versiones posteriores                      | FOLDERID \_ ProgramFiles, FOLDERID \_ PROGRAMFILESX86, FOLDERID \_ ProgramFilesX64, FOLDERID \_ ProgramFilesCommon, FOLDERID \_ ProgramFilesCommonX86 o FOLDERID \_ ProgramFilesCommonX64. Consulte [**KNOWNFOLDERID**](knownfolderid.md) para obtener información específica. |

    

     

-   No almacene los datos de usuario en la carpeta archivos de programa.

    Use la carpeta de datos apropiada para los datos que son comunes a todos los usuarios.

    

    | Sistema operativo                             | Location               |
    |----------------------------------------------|------------------------|
    | Windows XP, Windows Server 2003 y versiones anteriores | \_AppData comunes de CSIDL \_ |
    | Windows Vista y versiones posteriores                      | FOLDERID \_ ProgramData  |

    

     

    Use la carpeta de datos de usuario apropiada para los datos que pertenecen a un usuario determinado.

    

    | Sistema operativo                             | Location                                                   |
    |----------------------------------------------|------------------------------------------------------------|
    | Windows XP, Windows Server 2003 y versiones anteriores | CSIDL \_ AppData, CSIDL \_ personal y otros.               |
    | Windows Vista y versiones posteriores                      | FOLDERID \_ RoamingAppData, \_ documentos FOLDERID, etc. |

    

     

-   Si debe instalar en una ubicación distinta de la carpeta archivos de programa, asegúrese de establecer las listas de control de acceso (ACL) correctamente para que los usuarios no tengan acceso a partes inadecuadas del sistema de archivos. Los datos específicos de un usuario determinado deben tener una ACL que impida que cualquier otro usuario tenga acceso a él.
-   Al configurar las asociaciones de archivo, asegúrese de especificar correctamente la línea de comandos. Use una ruta de acceso completa y ajuste los elementos que contengan espacios en blanco entre comillas. Ajuste los parámetros de comando entre comillas independientes. De lo contrario, es posible que la cadena se analice incorrectamente y que la aplicación no se inicie correctamente. Aquí se muestran dos ejemplos de líneas de comandos con formato correcto.

    ```
    "C:\Program Files\MyApp\MyApp.exe" "%1" "%2"
    C:\MyAppDir\MyApp\MyApp.exe "%1"
    ```

    

> [!Note]  
> La ubicación de las carpetas de instalación estándar puede variar de un sistema a sistema. Para obtener la ubicación de una carpeta estándar en un sistema Windows Vista o posterior determinado, llame a [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) con el valor de [**KNOWNFOLDERID**](knownfolderid.md) adecuado. En Windows XP, Windows Server 2003 o sistemas anteriores, llame a [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) o [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con el valor de [**CSIDL**](csidl.md) adecuado.

 

## <a name="shlwapi"></a>Shlwapi

La API ligera de Shell (shlwapi) incluye una serie de funciones de manipulación de cadenas. El uso incorrecto de estas funciones puede conducir a cadenas truncadas inesperadamente sin notificación del truncamiento que se devuelve. En los casos siguientes, las funciones de shlwapi no deben usarse. Las funciones alternativas enumeradas, que suponen menos riesgos, deben usarse en su lugar.



| Shlwapi (función)                                                 | Función alternativa                                                                                             |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**StrCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw),[**StrNCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strncata)              | [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata) y funciones relacionadas             |
| [**StrCpy**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw), [ **StrCpyN**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw)             | [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**StringCbCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya) y funciones relacionadas         |
| [**wnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa), [ **wvnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa) | [**StringCchPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa), [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa) y funciones relacionadas |



 

Con funciones como [**PathRelativePathTo**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa) que devuelven una ruta de acceso de archivo, establezca siempre el tamaño del búfer en \_ caracteres de ruta de acceso máxima. Esto garantiza que el búfer sea lo suficientemente grande como para contener la ruta de acceso de archivo más grande posible, más un carácter nulo de terminación.

Para obtener más información sobre las funciones de cadena alternativas, vea [acerca de strsafe. h](../menurc/strsafe-ovw.md).

## <a name="autocomplete"></a>Autocompletar

No use la característica Autocompletar para contraseñas.

## <a name="shellexecute-shellexecuteex-and-related-functions"></a>ShellExecute, ShellExecuteEx y funciones relacionadas

Hay varias funciones de Shell que puede usar para iniciar aplicaciones: [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec)y [**SHCreateProcessAsUserW**](/windows/desktop/api/Shellapi/nf-shellapi-shcreateprocessasuserw). Asegúrese de proporcionar una definición inequívoca de la aplicación que se va a ejecutar.

-   Al proporcionar la ruta de acceso del archivo ejecutable, proporcione la ruta de acceso completa. No dependa del shell para buscar el archivo.
-   Si proporciona una cadena de línea de comandos que contiene espacios en blanco, incluya la cadena entre comillas. De lo contrario, el analizador podría interpretar un único elemento que contiene espacios como varios elementos.

## <a name="moving-and-copying-files"></a>Mover y copiar archivos

Una clave para la seguridad del sistema es la asignación correcta de las ACL. También puede usar archivos cifrados. Asegúrese de que cuando mueve o copia archivos, se les asigna la ACL correcta y que no se descifraron accidentalmente. Esto incluye el traslado de archivos a la **papelera de reciclaje**, así como del sistema de archivos. Usar [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) (Windows Vista o posterior) o [**SHFILEOPERATION**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) (Windows XP y versiones anteriores). No use [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile), que podría no establecer la ACL esperada para el archivo de destino.

## <a name="writing-secure-namespace-extensions"></a>Escribir extensiones de espacio de nombres seguras

Las extensiones de espacio de nombres de Shell son una manera eficaz y flexible de presentar datos al usuario. Sin embargo, pueden producir errores en el sistema si no se escriben correctamente. Algunos puntos clave que se deben tener en cuenta:

-   No asuma que los datos como imágenes tienen el formato correcto.
-   No suponga que \_ la ruta de acceso máxima es equivalente al número de *bytes* de una cadena. Es el número de *caracteres*.

## <a name="security-alerts"></a>Alertas de seguridad

En la tabla siguiente se enumeran algunas características que, si se usan incorrectamente, ponen en peligro la seguridad de las aplicaciones.



| Característica                                                                        | Mitigación                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), [ **ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) | Las búsquedas que dependen de la comprobación de una serie de ubicaciones predeterminadas para buscar un archivo específico se pueden usar en un ataque de suplantación de identidad. Use una ruta de acceso completa para asegurarse de que tiene acceso al archivo deseado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**StrCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw)                                                       | El primer argumento, *psz1*, debe ser lo suficientemente grande como para contener *psz2* y el cierre ' \\ 0 '; de lo contrario, podría producirse una saturación del búfer. En su lugar, utilice una de las siguientes alternativas. [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**StringCbCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna), [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa), [**StringCchCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)o [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa).                                                                                                                                                             |
| [**StrCatBuff**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa)                                               | No se garantiza que la cadena final esté terminada en NULL. En su lugar, utilice una de las siguientes alternativas. [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**StringCbCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna), [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa), [**StringCchCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)o [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa).                                                                                                                                                                                                                                  |
| [**StrCatChainW**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw)                                           | No se garantiza que la cadena final esté terminada en NULL. En su lugar, utilice una de las siguientes alternativas. [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)o [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa).                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**StrCpy**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw)                                                       | El primer argumento, *psz1*, debe ser lo suficientemente grande como para contener *psz2* y el cierre ' \\ 0 '; de lo contrario, podría producirse una saturación del búfer. En su lugar, utilice una de las siguientes alternativas. [**StringCbCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya), [**StringCbCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa), [**StringCbCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna), [**StringCbCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa), [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa), [**StringCchCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna)o [**StringCchCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa).                                                                                                                                             |
| [**StrCpyN**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw)                                                     | No se garantiza que la cadena copiada esté terminada en NULL. En su lugar, utilice una de las siguientes alternativas. [**StringCbCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya), [**StringCbCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa), [**StringCbCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna), [**StringCbCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa), [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa), [**StringCchCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna), [**StringCchCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa).                                                                                                                                                                                                                    |
| [**StrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa)                                                       | [**Strdup**](/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa) supone que *lpsz* es una cadena terminada en NULL. Además, no se garantiza que la cadena devuelta esté terminada en NULL. En su lugar, utilice una de las siguientes alternativas. [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**StringCbCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa), [**StringCbCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna), [**StringCbCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa), [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa), [**StringCchCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna)o [**StringCchCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa).                                                                                                                              |
| [**StrNCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strncata)                                                     | El primer argumento, *pszFront*, debe ser lo suficientemente grande como para contener *pszBack* y el cierre ' \\ 0 '; de lo contrario, podría producirse una saturación del búfer. Tenga en cuenta que el último argumento, *cchMax*, es el número de caracteres que se van a copiar en *pszFront*, no necesariamente el tamaño del *pszFront* en bytes. En su lugar, utilice una de las siguientes alternativas. [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**StringCbCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna), [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa), [**StringCchCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)o [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa). |
| [**wnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa)                                                 | No se garantiza que la cadena copiada esté terminada en NULL. En su lugar, utilice una de las siguientes alternativas. [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), [**StringCbPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfexa), [**StringCbVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfa), [**StringCbVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfexa), [**StringCchPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa), [**StringCchPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfexa), [**StringCchVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfa)o [**StringCchVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfexa).                                                                                                                                                                                 |
| [**wvnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa)                                               | No se garantiza que la cadena copiada esté terminada en NULL. En su lugar, utilice una de las siguientes alternativas. [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), [**StringCbPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfexa), [**StringCbVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfa), [**StringCbVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfexa), [**StringCchPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa), [**StringCchPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfexa), [**StringCchVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfa)o [**StringCchVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfexa).                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad de Microsoft](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[Centro para desarrolladores de seguridad](https://msdn.microsoft.com/security/)
</dt> <dt>

[Microsoft Solution Accelerators](/previous-versions/tn-archive/cc936627(v=technet.10))
</dt> <dt>

[TechCenter de seguridad](https://technet.microsoft.com/security/default.aspx)
</dt> <dt>

[Acerca de strsafe. h](../menurc/strsafe-ovw.md)
</dt> </dl>

 

 
