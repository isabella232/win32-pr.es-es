---
description: Para distribuir una aplicación habilitada para tinta en equipos que no ejecutan Windows Vista o Windows XP Tablet PC Edition 2005 (es decir, equipos que ejecutan Windows XP, Windows Server 2003 o Windows 2000), debe incluir los módulos de fusión mediante combinación necesarios en el programa de instalación.
ms.assetid: 97515703-0bf4-4230-ae35-181b48b70c40
title: Crear una instalación redistribuible
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1ad9b9ec8b10032d4a2bb44cca52e5c2f4178b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539441"
---
# <a name="creating-a-redistributable-setup"></a>Crear una instalación redistribuible

Para distribuir una aplicación habilitada para tinta en equipos que no ejecutan Windows Vista o Windows XP Tablet PC Edition 2005 (es decir, equipos que ejecutan Windows XP, Windows Server 2003 o Windows 2000), debe incluir los módulos de fusión mediante combinación necesarios en el programa de instalación.

El módulo de combinación Mstpcrt. MSM incluye todos los archivos, recursos, entradas del registro y lógica de configuración necesarias para Windows Installer instalar los archivos compartidos que otras plataformas requieren para ejecutar aplicaciones no administradas desarrolladas para Tablet PC. Mstpcrt. MSM lo consumen los archivos Windows Installer (. msi). En el caso de las aplicaciones que usan el objeto [**InkDivider**](inkdivider-class.md) , también debe redistribuir InkDiv. msm. En el caso de las aplicaciones que utilizan componentes administrados, también debe incluir los archivos de módulo de combinación para esos componentes administrados.

En la tabla siguiente se describen los archivos de módulo de combinación que se incluyen con el kit de desarrollo de software (SDK) de Windows XP Tablet PC Edition.



| Módulo de combinación redistribuible | Descripción                                                                                                                    | Archivos                                                       |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| InkDiv. MSM<br/>        | Instala la versión no administrada del objeto [**InkDivider**](inkdivider-class.md) .<br/>                                | InkDiv.dll<br/>                                       |
| Mstpcrt. MSM<br/>       | Instala los componentes no administrados de la plataforma de Tablet PC versión 1,0.<br/>                                            | Gdiplus.dll, InkEd.dll, Tpcps.dll, Wisptis.exe<br/>   |
| Msvcp60. MSM<br/>       | Instala los componentes del tiempo de ejecución de Microsoft Visual C++.<br/>                                                            | Msvcp60.dll<br/>                                      |
| Msvcrt. MSM<br/>        | Instala los componentes del tiempo de ejecución de Microsoft Visual C.<br/>                                                              | Msvcrt.dll<br/>                                       |
| Tpcman17. MSM<br/>      | Instala los componentes administrados del tiempo de ejecución de la plataforma de Tablet PC. Requiere que el archivo mstpcrt. MSM esté instalado.<br/> | Microsoft.Ink.dll, Microsoft.Ink.resources.dll<br/>   |
| iaCOM. MSM<br/>         | Instala los componentes de automatización de la API de InkAnalysis.<br/>                                                          | IACom.dll<br/>                                        |
| IACore. MSM<br/>        | Instala los componentes de la clase base de la API de InkAnalysis.<br/>                                                          | IACore.dll<br/> IALoader.dll<br/>               |
| IAWinFrm. MSM<br/>      | Instala los componentes de la biblioteca administrada de la API de InkAnalysis.<br/>                                                     | Microsoft.Ink.Analysis.dll<br/>                       |
| IAWinFX. MSM<br/>       | Instala los componentes de Windows Presentation Foundation de la API de InkAnalysis.<br/>                                     | IAWinFX.dll<br/>                                      |
| Journal. MSM<br/>       | Instala los componentes del lector del diario.<br/>                                                                             | Journal.dll<br/> Microsoft.ink.journal.dll<br/> |
| rtscom. MSM<br/>        | Instala los componentes de automatización del espacio de nombres StylusInput.<br/>                                                    | Rtscom.dll<br/>                                       |



 

> [!Note]  
> Para usar la funcionalidad de la Microsoft .NET Framework que se incluye en los módulos de combinación de los componentes administrados, debe tener instalado el Service Pack 2 de Framework en el equipo de destino.

 

## <a name="reduced-feature-set"></a>Conjunto reducido de características

Las aplicaciones habilitadas para tinta tratan los eventos del mouse como movimientos del lápiz para simular el trabajo con un lápiz de Tablet PC. Los usuarios pueden agregar tinta, borrar la tinta y guardar documentos de tinta. Sin embargo, el reconocimiento y los gestos no están disponibles para los usuarios que no sean los que ejecutan Windows XP Tablet PC Edition.

Mstpcrt. MSM no incluye el panel de entrada de Windows Journal o de Tablet PC.

El objeto [**PenInputPanel**](peninputpanel-class.md) no funciona en ningún sistema operativo además de Windows XP Tablet PC Edition.

## <a name="deployment"></a>Implementación

> [!Note]  
> Si su aplicación usa código administrado, también debe implementar el marco de trabajo. El marco de trabajo debe instalarse antes de que se instalen los ensamblados administrados de Tablet PC.

 

Para incluir Mstpcrt. MSM en un proyecto de instalación de .NET Microsoft Visual Studio:

1.  En el Explorador de soluciones, seleccione el proyecto de instalación.
2.  En el menú proyecto, haga clic en **Agregar** y, a continuación, en **módulo de combinación**.
    > [!Note]  
    > También puede obtener acceso al cuadro de diálogo **Agregar módulos** haciendo clic con el botón secundario en el nombre del proyecto de instalador en el explorador de soluciones, haciendo clic en **Agregar** y, a continuación, seleccionando **módulo de combinación**.

     

3.  En el cuadro de diálogo **Agregar módulos** , desplácese a y seleccione **Mstpcrt. MSM**.
4.  Haga clic en **Abrir**.

Mstpcrt. MSM se agrega al proyecto de instalación y aparece en la ventana Explorador de soluciones.

Windows Installer agrega los archivos contenidos en el módulo de combinación a la carpeta archivos de programa. Para usar estos archivos, los usuarios finales deben haber iniciado sesión con una cuenta que tenga acceso a la carpeta archivos de programa.

> [!Note]  
> Debe agregar la [acción SelfRegModules](../msi/selfregmodules-action.md) y las acciones de [acción de SelfUnregModules](../msi/selfunregmodules-action.md) a la secuencia de instalación. Las acciones de acción [MsiPublishAssemblies](../msi/msipublishassemblies-action.md) y [MsiUnpublishAssemblies](/windows/desktop/Msi/msiunpublishassemblies-action) reciben su orden en la secuencia de instalación de estas acciones.

 

 

