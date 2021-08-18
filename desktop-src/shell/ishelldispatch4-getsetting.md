---
description: 'Método IShellDispatch4.GetSetting: recupera una configuración de Shell global.'
ms.assetid: b9b1542c-8e25-4966-b3df-13bfbd9b28aa
title: Método IShellDispatch4.GetSetting (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.GetSetting
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ec31516f88dc9b79169a0272cfca735080e28aaebc81ac49cc7a8b083bc9377e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720859"
---
# <a name="ishelldispatch4getsetting-method"></a>Método IShellDispatch4.GetSetting

Recupera una configuración de Shell global.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = IShellDispatch4.GetSetting(
  lSetting
)
```


```VB

IShellDispatch4.GetSetting( _
  ByVal lSetting As long _
) As VARIANT_BOOL
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*lSetting* \[ En\]
</dt> <dd>

Tipo: **long**

Valor que especifica la configuración de Shell actual que se debe recuperar. Solo se puede recuperar una configuración en cada llamada. Este método reconoce los valores siguientes.

<dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF \_ AUTOCHECKSELECT** (0x00800000)


</dt> <dd>

**Windows Vista y versiones posteriores.** Estado de las **casillas Usar para seleccionar elementos.** Esta opción se habilita automáticamente cuando el sistema tiene configurado un dispositivo de entrada de lápiz.

</dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF \_ DESKTOPHTML** (0x00000200)


</dt> <dd>

No se usa.

</dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF \_ DONTPRETTYPATH** (0x00000800)


</dt> <dd>

Estado de la opción **Permitir todos los nombres en** mayúsculas. A Windows vista, esta opción de carpeta ya no está disponible.

</dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF \_ DOUBLECLICKINWEBVIEW** (0x00000080)


</dt> <dd>

Estado de la opción **Hacer doble clic para abrir un elemento (un solo clic para seleccionarlo).**

</dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF \_ FILTER** (0x00010000)


</dt> <dd>

No se usa.

</dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF \_ HIDDENFILEEXTS** (0x00000004)


</dt> <dd>

No se usa.

</dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF \_ HIDEICONS** (0x00004000)


</dt> <dd>

Estado de la presentación del icono en la vista de Windows explorador. Si esta opción está activa, no se muestra ningún icono en la vista de lista.

</dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF \_ ICONSONLY** (0x01000000)


</dt> <dd>

**Windows Vista y versiones posteriores.** El estado del nombre para mostrar que se muestra en la Windows explorador. Si esta opción está activa, los iconos se muestran en la vista de lista, pero no los nombres para mostrar.

</dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF \_ MAPNETDRVBUTTON** (0x00001000)


</dt> <dd>

Estado de la opción Mostrar unidad **de red de mapa en la barra de** herramientas. A Windows Vista, esta opción ya no está disponible.

</dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF \_ NOCONFIRMRECYCLE** (0x00008000)


</dt> <dd>

Estado de la opción de papelera de reciclaje cuadro de diálogo Mostrar **confirmación de eliminación del** servidor.

</dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF \_ NONETCRAWLING** (0x00100000)


</dt> <dd>

Estado de la opción **Buscar automáticamente carpetas de red e impresoras.** A Windows Vista, esta opción ya no está disponible.

</dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF \_ SEPPROCESS** (0x00080000)


</dt> <dd>

Estado de las ventanas **Iniciar carpeta en una opción de proceso** independiente.

</dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF \_ SERVERADMINUI** (0x00000004)


</dt> <dd>

No se usa.

</dd> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF \_ SHOWALLOBJECTS** (0x00000001)


</dt> <dd>

Estado de la opción **Archivos y carpetas ocultos.**

</dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF \_ SHOWATTRIBCOL** (0x00000100)


</dt> <dd>

Estado de la opción **Mostrar atributos de archivo en la vista de** detalles. A Windows Vista, esta opción ya no está disponible.

</dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF \_ SHOWCOMPCOLOR** (0x00000008)


</dt> <dd>

Estado de la opción Mostrar archivos **NTFS cifrados o comprimidos en color.**

</dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF \_ SHOWEXTENSIONS** (0x00000002)


</dt> <dd>

Estado de la opción **Ocultar extensiones para tipos de archivo** conocidos.

</dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF \_ SHOWINFOTIP** (0x00002000)


</dt> <dd>

Estado de la opción **Mostrar descripción emergente para elementos de escritorio y carpetas.**

</dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF \_ SHOWSTARTPAGE** (0x00400000)


</dt> <dd>

No se usa.

</dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF \_ SHOWSUPERHIDDEN** (0x00040000)


</dt> <dd>

Estado de la opción **Ocultar archivos de sistema operativo** protegidos.

</dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF \_ SHOWSYSFILES** (0x00000020)


</dt> <dd>

Estado de la opción **Archivos y carpetas ocultos.** En Windows Vista y versiones posteriores, esto equivale a SSF \_ SHOWALLOBJECTS. En versiones de Windows antes Windows Vista, este valor hacía referencia al estado de la opción No mostrar archivos **y carpetas ocultos.**

</dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF \_ SHOWTYPEOVERLAY** (0x02000000)


</dt> <dd>

**Windows Vista y versiones posteriores.** Estado de la opción **Mostrar icono de archivo en miniaturas.** Si esta opción está activa, se aplica una superposición de tipo de archivo cuando un archivo proporciona una representación en miniatura.

</dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF \_ SORTCOLUMNS** (0x00000010)


</dt> <dd>

No se usa.

</dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF \_ STARTPANELON** (0x00200000)


</dt> <dd>

El estado de la Windows de visualización XP, que selecciona entre el Windows XP y el estilo clásico. A Windows Vista, esta opción ya no está disponible.

</dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF \_ WEBVIEW** (0x00020000)


</dt> <dd>

Estado de la opción **Mostrar como vista web**. A Windows Vista, esta opción ya no está disponible.

</dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF \_ WIN95CLASSIC** (0x00000400)


</dt> <dd>

Estado de la opción **Estilo** clásico. A Windows Vista, esta opción ya no está disponible.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **VARIANT \_ BOOL \***

Establezca en **true** si la configuración existe; de lo contrario, **false**.

### <a name="vb"></a>VB

Tipo: **VARIANT \_ BOOL \***

Establezca en **true** si la configuración existe; de lo contrario, **false**.

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso de **GetSetting** para JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JavaScript">
    function fnIShellDispatch4GetSettingJ()
    {
        var objIShellDispatch4 = new ActiveXObject("Shell.Application");
        var vReturn;
        var ssfSHOWALLOBJECTS = 1;

        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS);
        alert(vReturn);
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnIShellDispatch4GetSettingVB()
        dim objIShellDispatch4
        
        set objIShellDispatch4 = CreateObject("Shell.Application")
        if (not objIShellDispatch4 is nothing) then
            dim vReturn
            dim ssfSHOWALLOBJECTS
            
            ssfSHOWALLOBJECTS = 1
            vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
            alert(vReturn)
        end if
        set objIShellDispatch4 = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub fnIShellDispatch4GetSetting()
    Dim objIShellDispatch4 As Shell
    
    Set objIShellDispatch4 = New Shell
    If (Not objIShellDispatch4 Is Nothing) Then
        Dim vReturn As Variant
        Dim ssfSHOWALLOBJECTS As Long
        
        ssfSHOWALLOBJECTS = 1
        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
        Debug.Print vReturn
    End If
    Set objIShellDispatch4 = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 6.0 o posterior)</dt> </dl> |



 

 




